# Run Blocks

Run Blocks is a powerful and intuitive web application that allows you to create, run, and test JavaScript code blocks in a dynamic and interactive environment. With Run Blocks, you can easily organize your code into projects, create code blocks, establish relationships between them, and view the results of your code execution in real-time.

## Features

1. **Project Management**: Run Blocks provides a seamless project management system. You can create multiple projects, each containing its own set of code blocks. The project selector allows you to switch between projects effortlessly.

2. **Dynamic Code Blocks**: Create code blocks dynamically on an infinite canvas. Each code block represents a JavaScript file and can be easily moved, resized, and connected to other code blocks.

3. **Code Editor**: Run Blocks integrates a powerful code editor with syntax highlighting, code completion, and error highlighting. The editor supports JavaScript and provides a smooth coding experience.

4. **Code Block Relationships**: Establish relationships between code blocks by creating import statements. When you add a sub-block to a code block, Run Blocks automatically generates the necessary import statement and visually connects the blocks with arrows.

5. **Real-time Execution**: Execute your JavaScript code in real-time and view the results instantly. Run Blocks captures and displays the output, including console logs, errors, and return values, providing a comprehensive view of your code's behavior.

6. **Function and Method Tracking**: Run Blocks tracks the execution of functions and methods within your code. It captures the arguments passed to each function, the return values, and the order of execution, giving you deep insights into your code's flow.

7. **Variable Monitoring**: Monitor the values of variables throughout your code execution. Run Blocks captures the initial values and any modifications made to variables, allowing you to inspect their state at different points in your code.

8. **Class and Object Tracking**: Run Blocks provides detailed tracking of classes, objects, and their methods. It captures class instantiations, method invocations, and property access, giving you a clear understanding of your object-oriented code.

9. **Scope Analysis**: Gain insights into the scope of your variables and functions. Run Blocks identifies variables declared in the global scope and within specific code blocks, helping you understand the accessibility and lifetime of your variables.

10. **Error Handling and Logging**: Run Blocks implements comprehensive error handling and logging mechanisms. It captures and displays errors that occur during code execution, providing valuable information for debugging and troubleshooting.

11. **Breakpoints and Stepping**: Debug your code effectively with breakpoints and stepping capabilities. Set breakpoints at specific lines and step through your code execution to identify issues and understand the program flow.

12. **Code Optimization Suggestions**: Run Blocks analyzes your code and provides optimization suggestions. It identifies potential performance bottlenecks, suggests best practices, and offers guidance on improving code efficiency.

13. **Collaborative Editing**: Collaborate with your team in real-time. Run Blocks allows multiple users to work on the same project simultaneously, with live updates and conflict resolution.

14. **Version Control Integration**: Seamlessly integrate Run Blocks with popular version control systems like Git. Commit your code changes, create branches, and manage your project's history directly within the application.

15. **Code Snippets and Templates**: Boost your productivity with code snippets and templates. Run Blocks provides a library of reusable code snippets and project templates that you can easily insert into your code blocks.

16. **Import and Export**: Import existing JavaScript files into your Run Blocks projects. Export your projects as standalone JavaScript files or as a packaged project for sharing and collaboration.

17. **Testing and Assertion**: Write and run tests directly within Run Blocks. The application supports popular testing frameworks and provides an intuitive interface for defining test cases and assertions.

18. **Performance Profiling**: Profile the performance of your code with Run Blocks' built-in profiling tools. Identify performance bottlenecks, measure execution times, and optimize your code for better efficiency.

19. **Documentation Generation**: Automatically generate documentation for your code blocks. Run Blocks extracts comments and annotations from your code and creates structured documentation that can be easily shared and maintained.

20. **Integration with External Tools**: Integrate Run Blocks with external tools and services. Connect with databases, APIs, and third-party libraries to extend the functionality of your code blocks and build comprehensive applications.

## Installation

To run Run Blocks locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your-repo/run-blocks.git`
2. Navigate to the project directory: `cd run-blocks`
3. Install the dependencies: `npm install`
4. Create a `.env` file based on the provided `.env.example` and configure the necessary environment variables.
5. Start the development server: `npm run dev`
6. Open your browser and visit `http://localhost:3000` to access Run Blocks.

## Technologies Used

Run Blocks is built using the following technologies and libraries:

- **Nuxt 3**: A powerful Vue.js framework for building server-side rendered and static web applications.
- **Vue.js**: A progressive JavaScript framework for building user interfaces.
- **Vue Composition API**: A set of APIs for creating reusable and flexible components in Vue.js.
- **TypeScript**: A typed superset of JavaScript that compiles to plain JavaScript.
- **vue-infinite-canvas**: A Vue.js component for creating infinite canvases with panning and zooming capabilities.
- **Monaco Editor**: A powerful code editor component with syntax highlighting, code completion, and error highlighting.
- **Pinia**: A state management library for Vue.js applications, focusing on simplicity and developer experience.
- **MariaDB**: A high-performance, open-source relational database management system, used for server-side persistent data storage.
- **Prisma**: A modern database toolkit for TypeScript and Node.js, providing an intuitive and type-safe way to interact with the database.
- **Express.js**: A fast and minimalist web application framework for Node.js, used for building the server-side API.
- **Inversify**: A lightweight and powerful inversion of control container for TypeScript and JavaScript.
- **Winston**: A logger for just about everything in JavaScript.
- **Jest**: A delightful JavaScript testing framework with a focus on simplicity.
- **ESLint**: A pluggable and configurable linter tool for identifying and reporting on patterns in JavaScript code.

## Server-Side Persistent Data Storage with MariaDB

To implement server-side persistent data storage, Run Blocks utilizes MariaDB as the database management system. MariaDB is a reliable and scalable relational database that ensures data integrity and provides efficient querying capabilities.

The integration with MariaDB is achieved through the following steps:

1. **Database Setup**: A MariaDB database is set up on the server to store the application's data. The database schema is designed to accommodate the various entities and relationships required by Run Blocks, such as projects, code blocks, and execution results.

2. **Prisma Integration**: Prisma, a modern database toolkit, is used to interact with the MariaDB database from the server-side code. Prisma provides an intuitive and type-safe way to define the database schema, generate database migrations, and perform database operations.

3. **Data Models**: The data models for Run Blocks are defined using Prisma's schema definition language. These models represent the structure and relationships of the data stored in the MariaDB database. The models include entities such as `Project`, `CodeBlock`, `Execution`, and `Result`.

4. **API Endpoints**: Express.js is used to build the server-side API endpoints that handle data persistence operations. The API endpoints are responsible for creating, reading, updating, and deleting data in the MariaDB database. Prisma is used within these endpoints to interact with the database and perform the necessary operations.

5. **Data Retrieval and Synchronization**: When a user interacts with Run Blocks, the application communicates with the server-side API to retrieve and synchronize data. The API endpoints fetch the required data from the MariaDB database using Prisma and return it to the client-side application. This ensures that the user always has access to the latest data and can seamlessly switch between different devices or sessions.

6. **Real-time Updates**: To provide real-time updates and collaboration features, Run Blocks uses WebSocket communication. When changes are made to the data on the server-side, such as creating a new code block or updating an existing one, the server sends real-time updates to all connected clients. This ensures that all users have a synchronized view of the data and can collaborate effectively.

7. **Data Backup and Restoration**: Regular backups of the MariaDB database are performed to ensure data durability and protect against data loss. Backup processes are automated and scheduled to create periodic snapshots of the database. In case of any data corruption or system failure, the database can be restored from the latest backup to minimize data loss and ensure business continuity.

By leveraging MariaDB for server-side persistent data storage, Run Blocks provides a robust and reliable foundation for storing and managing application data. The combination of Prisma and Express.js simplifies the interaction with the database and enables seamless data persistence and retrieval.

## Conclusion

Run Blocks is a powerful and feature-rich web application for creating, running, and testing JavaScript code blocks. With its intuitive interface, real-time collaboration, and extensive set of features, Run Blocks simplifies the process of writing and debugging code.

The combination of Nuxt 3, Vue.js, Pinia, MariaDB, and other modern technologies enables Run Blocks to deliver a seamless and efficient user experience. The server-side persistent data storage with MariaDB ensures that user data is securely stored and can be accessed from anywhere.

We hope that Run Blocks becomes an invaluable tool in your development workflow and helps you streamline your coding process. If you have any further questions or feedback, please don't hesitate to reach out to our support team.

Thank you for choosing Run Blocks!

## Project Structure

The project structure of Run Blocks is organized as follows:

```
run-blocks/
  ├── assets/
  │   └── ...
  ├── components/
  │   ├── CodeBlock.vue
  │   ├── CodeEditor.vue
  │   ├── InfiniteCanvas.vue
  │   ├── ProjectSelector.vue
  │   └── ...
  ├── layouts/
  │   └── default.vue
  ├── middleware/
  │   └── ...
  ├── pages/
  │   └── index.vue
  ├── plugins/
  │   └── ...
  ├── services/
  │   ├── projectService.ts
  │   ├── codeBlockService.ts
  │   ├── executionService.ts
  │   └── ...
  ├── store/
  │   ├── index.ts
  │   ├── projects.ts
  │   ├── codeBlocks.ts
  │   └── ...
  ├── utils/
  │   └── ...
  ├── .env
  ├── .env.example
  ├── .eslintrc.js
  ├── .gitignore
  ├── jest.config.js
  ├── nuxt.config.ts
  ├── package.json
  ├── README.md
  ├── tsconfig.json
  └── ...
```

- `assets/`: Contains static assets such as images, fonts, and stylesheets.
- `components/`: Contains reusable Vue.js components used throughout the application.
- `layouts/`: Contains the main layout components for the application.
- `middleware/`: Contains custom middleware functions.
- `pages/`: Contains the main pages of the application.
- `plugins/`: Contains custom plugins and extensions.
- `services/`: Contains TypeScript services for handling business logic and data manipulation.
- `store/`: Contains Vuex store modules for managing application state.
- `utils/`: Contains utility functions and helper modules.

## Getting Started

To start using Run Blocks, follow these steps:

1. Create a new project by clicking the "New Project" button in the project selector.
2. Give your project a name and click "Create".
3. You will be redirected to the project's infinite canvas.
4. Click the "Add Code Block" button in the toolbar to create a new code block.
5. Double-click the code block to open the code editor.
6. Write your JavaScript code in the editor and save your changes.
7. To add a sub-block, click the "Add Sub-block" button in the code block's header.
8. Repeat steps 4-7 to create additional code blocks and establish relationships between them.
9. Click the "Run" button in the toolbar to execute your code and view the results.
10. Use the toolbar buttons to control the execution flow, set breakpoints, and monitor variables.

## Contributing

We welcome contributions to Run Blocks! If you would like to contribute, please follow these steps:

1. Fork the repository on GitHub.
2. Create a new branch from the `main` branch.
3. Make your changes and commit them with descriptive commit messages.
4. Push your changes to your forked repository.
5. Submit a pull request to the `main` branch of the original repository.

Please ensure that your code adheres to the project's coding standards and includes appropriate tests.

## License

Run Blocks is open-source software licensed under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute the code as per the terms of the license.

## Contact

If you have any questions, suggestions, or feedback, please feel free to contact us at [charl@webally.co.za](mailto:charl@webally.co.za). We appreciate your input and support!

Happy coding with Run Blocks!
