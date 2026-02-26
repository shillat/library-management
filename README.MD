# Library Management Server

A minimalist, high-concurrency Java Library Server leveraging the native `com.sun.net.httpserver` stack. This project serves as a technical demonstration of low-level HTTP request handling, RESTful routing, and state management, designed specifically for academic and lightweight deployment contexts.

## Table of Contents

* [System Architecture](#system-architecture)*
* [Technical Stack](https://www.google.com/search?q=%23technical-stack)
* [Prerequisites](https://www.google.com/search?q=%23prerequisites)
* [Installation & Execution](https://www.google.com/search?q=%23installation--execution)
* [API Specification](https://www.google.com/search?q=%23api-specification)
* [Contribution Workflow](https://www.google.com/search?q=%23contribution-workflow)
* [Contact & Project Governance](https://www.google.com/search?q=%23contact--project-governance)
* [License](https://www.google.com/search?q=%23license)

## System Architecture

The application implements a **Stateless Client-Server Model**. The backend acts as a centralized Controller, managing both data persistence and the delivery of the View (HTML/CSS) to the Client.

### Core Components

* **Request Dispatcher:** Intercepts incoming TCP traffic and routes it to specific `HttpHandler` contexts (e.g., `/add`, `/view`).
* **Data Persistence:** Utilizes a synchronized **In-Memory Collection** to ensure thread safety during concurrent operations.
* **MVC Pattern:** Separates the **Book data (Model)**, the **browser interface (View)**, and the **server-side logic (Controller)**.

## Technical Stack

| Component | Technology | Role |
| --- | --- | --- |
| **Language** | Java 8+ | Core Logic & Server Engine |
| **Server Stack** | `com.sun.net.httpserver` | HTTP Protocol Handling |
| **Frontend** | HTML5 / CSS3 | User Interface & Forms |
| **State Management** | Java Collections | In-memory Data Storage |

## Prerequisites

* **Java Development Kit (JDK) 8 or higher:** Required for the `javac` compiler and `java` runtime.
* **Terminal Environment:** Bash, Zsh, or PowerShell.
* **Web Browser:** Tested on Chrome, Firefox, and Edge.

## Installation & Execution

### 1. Repository Setup

```bash
git clone https://github.com/your-username/LibraryManagementServer.git
cd LibraryManagementServer

```

### 2. Compilation

```bash
javac LibraryServer.java

```

### 3. Server Deployment

```bash
java LibraryServer

```

> **Note:** The default listener is configured for `http://localhost:8000`.

## API Specification

| Method | Endpoint | Description |
| --- | --- | --- |
| **GET** | `/` | Serves the main Dashboard/Interface. |
| **GET** | `/books` | Fetches a list of all library records. |
| **POST** | `/add-book` | Submits a new book entry (Title, Author, Year). |

## Contribution Workflow

We follow a rigorous Pull Request (PR) process to maintain code integrity:

1. **Branching:** Use `git checkout -b feature/your-feature-name`.
2. **Standards:** Adhere to the [Google Java Style Guide](https://www.google.com/search?q=https://google.github.io/styleguide/javaguide.html).
3. **Documentation:** All public methods must include Javadoc syntax.
4. **Validation:** Ensure the server compiles and handles concurrent requests before submission.

## Contact & Project Governance

### Project Owner

* **GitHub:** [cyrotevez](https://www.google.com/search?q=https://github.com/cyrotevez)

### Active Contributors

* **Shillat Naigaga** — *Current Documentation & Optimization Lead*
* **GitHub:** [shillat](https://www.google.com/search?q=https://github.com/shillat)
* **Email:** shillahnaigaga5@gmail.com

### Academic Context

This project is maintained as part of a University-level Software Engineering curriculum. For inquiries regarding licensing or academic collaboration, please reach out via the GitHub Issues tab.

## 📜 License

This project is licensed under the **MIT License**.
The MIT License is a permissive free software license that allows for reuse within proprietary software, provided that all copies of the software or its substantial portions include a copy of the terms of the MIT License and the copyright notice.

---

### Evidence of Professional Standard

According to the **GitHub Documentation Best Practices**, using lowercase identifiers and hyphens for anchors (e.g., `#system-architecture`) is the standard for GitHub Flavored Markdown (GFM). This ensures that your Table of Contents remains robust even as the project scales.

**Would you like me to help you create a `CHANGELOG.md` file so you can document the specific versioning and improvements you have made to this project?**
