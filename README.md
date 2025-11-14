# logos_platform
A web app for symbolic intelligence training, created for personal learning purposes. The core idea is to allow the user to insert data about themself and get insights from the app. A self-hacking app.

## Architecture

The app is built using the following technologies:
- **Frontend**: HTML, CSS, a little JavaScript
- **Backend**: Just SWI-Prolog (no SQL or noSQL databases, no ORMs, no Redis), a knowledge base which handles everything from user authentication to data storage and retrieval, to business logic and data processing.
- **Containerization**: Docker is used to containerize the application for easy deployment and scalability.
- **Web Server**: SWI-Prolog's built-in HTTP server is used to handle web requests and serve the frontend.
- **Data Storage**: Data is stored in Prolog's native format, leveraging its powerful pattern matching and logical inference capabilities.
- **APIs**: RESTful APIs are implemented using SWI-Prolog to facilitate communication between the frontend and backend.
- **Authentication**: User authentication is managed within the Prolog backend, ensuring secure access to user data.
- **Deployment**: The application can be deployed on any server that supports Docker, making it easy to set up and run in various environments.
- **Version Control**: Git is used for version control, allowing for collaborative development and easy tracking of changes.
- **Testing**: Unit tests and integration tests are written in Prolog to ensure the reliability and correctness of the application.
- **Documentation**: Comprehensive documentation is provided to help users understand the architecture, setup, and usage of the application.


