# Boilerplate Project Messageboard

This project is an implementation of a message board as part of the freeCodeCamp Information Security and Quality Assurance Projects curriculum. It allows users to post messages, reply to others, and delete or report posts or replies. It's built with Node.js and Express, with support for CORS and secure HTTP headers implemented via Helmet.js.

## Installation

To get started with this project, clone this repository and install the dependencies.

```
git clone https://github.com/yourusername/boilerplate-project-messageboard.git
cd boilerplate-project-messageboard
npm install
```

## Usage

Once the installation is complete, you can start the server with the following command:

```
npm start
```

This will start the server on the default port 3000. You can access the project in your web browser at `http://localhost:3000`.

## Running Tests

This project comes with functional tests. To run these tests, you need to set the `NODE_ENV` environment variable to `test`. This can be done as follows:

```
NODE_ENV=test npm test
```

## API Documentation

### Threads

- **POST** `/api/threads/:board` - Create a new thread on a specific board.
- **GET** `/api/threads/:board` - View the 10 most recent threads on a board with only the 3 most recent replies each.
- **DELETE** `/api/threads/:board` - Delete a thread if the correct password is provided.
- **PUT** `/api/threads/:board` - Report a thread.

### Replies

- **POST** `/api/replies/:board` - Post a reply to a thread on a specific board.
- **GET** `/api/replies/:board` - View a single thread with all replies (excluding password and report fields).
- **DELETE** `/api/replies/:board` - Delete a reply from a thread if the correct password is provided.
- **PUT** `/api/replies/:board` - Report a reply on a thread.

## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.

Please ensure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
