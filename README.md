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
- **Continuous Integration/Continuous Deployment (CI/CD)**: Automated pipelines are set up to streamline the development and deployment process, ensuring that new features and updates are delivered efficiently.
- **Monitoring and Logging**: Tools are integrated to monitor the application's performance and log importante events, aiding in maintenance and troubleshooting.
- **Scalability**: The architecture is designed to be scalable, allowing for easy expansion of features and handling of increased user load as needed.
- **Security**: Best practices are followed to ensure the security of user data and the overall application, including data encryption and secure coding standards.
- **User Interface (UI)**: The frontend is designed to be minimalist, focusing on usability and simplicity to enhance the user experience.
- **Facts Analysis**: Prolog's logical reasoning capabilities are utilized to analyze user facts and provide meaningful insights and recommendations.
- **Extensibility**: The architecture allows for easy addition of new features and functionalities as the application evolves.
- **Community Support**: Leveraging the SWI-Prolog community for support and resources to enhance the development process.
- **Learning Focus**: The project serves as a learning platform for exploring web development from scratch using Prolog, emphasizing hands-on experience and experimentation.

## Design details

### Frontend

The frontend is designed to be minimalist, focusing on usability and simplicity. It consists of HTML pages styled with CSS, with minimal JavaScript for interactivity. The main components include:

- **Home Page**: A landing page that introduces the app and its purposes.
- **User Dashboard**: A personalized dashboard where users can view, add, remove, manage, elaborate on their facts, and see insights generated from their data.
- **Fact Management**: Interfaces for users to input new facts about themselves, edit existing ones, and delete facts they no longer want to keep.
- **Insights Page**: A section where users can see analyses and insights derived from their facts, presented in a clear and understandable manner.

### Bakcend

The backend is built entirely using SWI-Prolog, leveraging its strengths in logical reasoning and pattern matching. Key components include:

- **HTTP Server**: Utilizes SWI-Prolog's built-in HTTP server to handle incoming requests and serve the frontend.
- **User Authentication**: Manages user registration, login, and session management to ensure secure access to user data.
- **Facts Storage**: Stores user facts in Prolog's native format within the knowledge base, allowing for efficient retrieval and manipulation.
- **Business Logic**: Implements the core functionality of the app, including fact management and insights generation.
- **APIs**: Provides RESTful APIs for communication between the frontend and the backend, enabling dynamic interactions and facts updates.
- **Facts Processing**: Analyzes user facts using Prolog's logical inference capabilities to generate insights and recommendations.
- **Data Security**: Ensures that user data is handled securely, following best practices for data protection and privacy.
- **Error Hangling**: Implements robust error handling to manage unexpected situations and provide meaningful feedback to users.

### Containerization

The application is containerized using Docker, which allows for easy deployment and scalability. The Docker setup includes:

- **Dockerfile**: Defines the environment for the application, including the installation of SWI-Prolog and necessary dependencies.
- **Docker Compose**: Manages multi-container setups if needed, allowing for easy orchestration of services.
- **Environment Configuration**: Uses environment variables to configure the application settings, making it adaptable to different deployment environments.
- **Port Mapping**: Configures port mappings to expose the application to the host machine for access.
- **Volume Management**: Sets up volumes for persistent data storage, ensuring that user data is retained across container restarts.
- **Networking**: Configures networking settings to allow communication between containers if multiple services are used.
- **Build and Deployment Scripts**: Provides scripts for building and deploying the Docker containers, streamlining the setup process.
- **Documentation**: Includes documentation on how to build, run, and manage the Docker containers for the application.

### Deployment

The application can be deployed on any server that supports Docker. The deployment process includes:
- **Server Setup**: Preparing the server environment, including installing Docker and Docker Compose.
- **Container Deployment**: Using Docker commands to build and run the application containers on the server.
- **Domain Configuration**: Setting up domain names and SSL certificates if needed for secure access.
- **Monitoring**: Implementing monitoring tools to track the application's performance and health post-deployment.
- **Backup Strategies**: Establishing backup procedures to safeguard user data and application state.
- **Scaling**: Planning for scalability to handle increased user load, including strategies for load balancing and resource allocation.
- **Maintenance**: Setting up routines for regular maintenance, updates, and security.
- **Documentation**: Providing clear documentation for the deployment process to assist in future deployments and troubleshooting.

### How does the knowledge base replaces traditional databases?

The knowledge base in SWI-Prolog serves as the primary data storage mechanism, replacing traditional databases by leveraging Prolog's inherent capabilities for data representation and manipulation. Here's how it works:

- **Data Representation**: User facts are represented as Prolog predicates, allowing for a flexible and dynamic way to store information without the need for predefined schemas.
- **Logical Inference**: Prolog's logical reasoning capabilities enable complex queries and data retrieval based on relationships and conditions defined within the knowledge base.
- **Dynamic Updates**: Facts can be easily added, modified, or removed in real-time, allowing for a responsive and interactive user experience.
- **NoSQL-like Flexibility**: The knowledge base functions similarly to a NoSQL database, where data can be stored in a non-relational format, making it adaptable to various types of user information.
- **Built-In Querying**: Prolog's querying capabilities allow for efficient data retrieval without the need for complex SQL queries, simplifying the interaction between the frontend and the backend.
- **Reduced Overhead**: By using Prolog's native data handling, the application avoids the overhad of managing separate databases and ORMs, leading to a more streamlined architecture.
- **Integrated Business Logic**: The knowledge base not only stores data but also encapsulates business logic, enabling seamless integration between data management and application functionality.
- **Security**: Data security is managed within the Prolog environment, ensuring that user information is protected through controlled access and manipulation.
- **Scalability**: The knowledge base can be scaled as needed, with Prolog's efficient handling of large datasets and complex queries.
- **Ease of Development**: Developers can focus on building application features without worrying about database management, leading to faster development cycles and easier maintenance.

### How does the knowledge base makes caching with Redis useless?

The knowledge base in SWi-Prolog eliminates the need for caching solutions like Redis by efficiently managing data retrieval and processing within its logical framework. Here's how it achieves this:
- **Efficient Data Access**: Prolog's pattern matching and logical inference capabilities allow for quick data retrieval directly from the knowledge base, reducing the need for intermediate caching layers.
- **In-Memory Processing**: The knowledge base operates in-memory, enabling fast access to user facts and reducing latency associated with external caching systems.
- **Dynamic Fact Management**: Facts can be added, modified, or removed on-the-fly, allowing for real-time updates without the need for cache invalidation strategies.
- **Integrated Querying**: Prolog's built-in querying mechanism enables efficient data retrieval based on complex conditions, minimizing the need for pre-cached results.
- **Reduced Complexity**: By handling data storage and retrieval within the knowledge base, the application avoids the added complexity of managing a separate caching layer, simplifying the architecture.
- **Consistent Data**: Since all data operations occur within the knowledge base, there is no risk of cache inconsistencies, ensuring that users always access the most up-to-date information.
- **Optimized Performance**: The knowledge base is optimized for performance, allowing for rapid data access and processing without the overhead of external caching solutions.
- **Simplified Development**: Developers can focus on building application features without the need to implement and maintain caching logic, leading to faster development cycles and easier maintenance.
- **Scalability**: The knowledge base can handle increased data loads and user requests efficiently, reducing the needs for additional caching mechanisms as the application scales.
- **Resource Efficiency**: By eliminating the need for Redis, the application reduces resource consumption, leading to lower operational costs and improved performance.

### How does the knowledge base handles persistency in an efficient way?

The knowledge base in SWI-Prolog handles persistency efficiently through several mechanisms that ensure data durability and integrity without the need for traditional database systems. Here's how it achieves this:

- **File-Based Storage**: User facts and data can be serialized and stored in Prolog's native file format, allowing for easy saving and loading of the knowledge base as needed.
- **Incremental Saving**: Changes to the knowledge base can be saved incrementally, reducing the overhead of writing large datasets to disk and improving performances.
- **Snapshotting**: The knowledge base can create snapshots of its state at specific intervals, enabling quick recovery in case of failures or crashes.
- **Efficient Loading**: Prolog's built-in mechanisms allow for efficient loading of data, minimizing startup times and ensuring that the application can quickly access user facts.
