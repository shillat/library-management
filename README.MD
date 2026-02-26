# Library Management Server

A minimalist, high-concurrency **Java Library Server** leveraging the native `com.sun.net.httpserver` stack. This project serves as a technical demonstration of low-level HTTP request handling, RESTful routing, and state management within a single-threaded environment, designed specifically for educational and lightweight deployment contexts.



## ## Table of Contents

1. [System Architecture](https://www.google.com/search?q=%23system-architecture)
2. [Technical Stack](https://www.google.com/search?q=%23technical-stack)
3. [Prerequisites](https://www.google.com/search?q=%23prerequisites)
4. [Installation & Execution](https://www.google.com/search?q=%23installation--execution)
5. [API Specification](https://www.google.com/search?q=%23api-specification)
6. [Contribution Workflow](https://www.google.com/search?q=%23contribution-workflow)
7. [Contact & Project Governance](https://www.google.com/search?q=%23contact--project-governance)



## ## System Architecture

The application implements a **Stateless Client-Server Model**. The backend acts as a centralized Controller, managing both the data persistence and the delivery of the View (HTML/CSS) to the Client.

### Core Components

* **Request Dispatcher**: Intercepts incoming TCP traffic and routes it to specific `HttpHandler` contexts (e.g., `/add`, `/view`).
* **Data Persistence**: Utilizes a synchronized In-Memory Collection to ensure thread safety when multiple users interact with the library catalog.
* **Model-View-Controller (MVC) Pattern**: While lightweight, the server logic separates the `Book` data (Model), the browser interface (View), and the server-side logic (Controller).



## ## Technical Stack

| Component | Technology | Role |
| --- | --- | --- |
| **Language** | Java 8+ | Core Logic & Server Engine |
| **Server Stack** | `com.sun.net.httpserver` | HTTP Protocol Handling |
| **Frontend** | HTML5 / CSS3 | User Interface & Forms |
| **State Management** | Java Collections | In-memory Data Storage |



## ## Prerequisites

* **Java Development Kit (JDK) 8 or higher**: Essential for the `javac` compiler and `java` runtime.
* **Terminal Environment**: Bash, Zsh, or PowerShell.
* **Standard Web Browser**: Tested on Chrome, Firefox, and Safari.



## ## Installation & Execution

### 1. Repository Setup

Clone the repository to your local development environment:

```bash
git clone https://github.com/your-username/LibraryManagementServer.git
cd LibraryManagementServer

```

### 2. Compilation

Compile the primary server class. This will generate the necessary `.class` bytecode:

```bash
javac LibraryServer.java

```

### 3. Server Deployment

Initialize the server instance:

```bash
java LibraryServer

```

*The default listener is configured for **`http://localhost:8000`**.*



## ## API Specification

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/` | Serves the main Dashboard/Interface. |
| `GET` | `/books` | Fetches a list of all library records in JSON/HTML format. |
| `POST` | `/add-book` | Submits a new book entry (Title, Author, Year) to the collection. |



## ## Contribution Workflow

We follow a rigorous **Pull Request (PR)** process to maintain code integrity.

1. **Branching**: Create a feature branch using `git checkout -b feature/your-feature-name`.
2. **Standards**: Adhere to [Google Java Style Guide](https://www.google.com/search?q=https://google.github.io/styleguide/javaguide.html).
3. **Documentation**: Ensure all public methods are documented using standard Javadoc syntax.
4. **Testing**: Verify that the server compiles and handles concurrent requests before submission.



## ## Contact & Project Governance

### Primary Owner

* **Project Owner's Name**: [Owner's Name]
* **GitHub**: cyrotevez(https://www.google.com/search?q=https://github.com/cyrotevez)
* **Email**: [Email]

We welcome Contributions. Below is a list of active contributers.

### Primary Contributors

* **Active Contributor**: Shillat Naigaga — *Current Documentation & Optimization Lead*
* **GitHub**: shillat(https://www.google.com/search?q=https://github.com/shillat)
* **Email**: shillahnaigaga5@gmail.com



### Academic Context

This project is maintained as part of a University-level Software Engineering curriculum. For inquiries regarding licensing or academic collaboration, please reach out via the GitHub Issues tab.

## 📜 License

This project is licensed under the **MIT License**. 

The MIT License is a permissive free software license that allows for reuse within proprietary software, provided that all copies of the software or its substantial portions include a copy of the terms of the MIT License and the copyright notice.

See the [LICENSE](LICENSE) file for the full text.



