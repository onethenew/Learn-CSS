# Learn-CSS

[![GitHub license](https://img.shields.io/github/license/onethenew/Learn-CSS?style=flat-square)](LICENSE)
[![GitHub package.json version](https://img.shields.io/github/package-json/v/onethenew/Learn-CSS?style=flat-square)](package.json)

A foundational web project designed for learning and practicing modern web development fundamentals using HTML, CSS, JavaScript, and Vite.

## Overview

This project serves as a minimal boilerplate to explore core web technologies and the Vite build tool. It provides a simple interactive counter application, making it an excellent starting point for beginners to understand how HTML, CSS, and JavaScript integrate within a modern development environment.

**Key Value Proposition:**
- **Rapid Setup:** Get a development server running in seconds with Vite.
- **Hands-on Learning:** Directly modify HTML, CSS, and JavaScript to see immediate results.
- **Modern Tooling:** Experience a contemporary web development workflow.

**Target Audience:**
Web development beginners, students, or anyone looking for a quick sandbox to experiment with front-end technologies and Vite.

**Current Status:**
This is a basic learning project, primarily for educational and experimental purposes.

## Features

*   **Vite-Powered Development Server:** Enjoy lightning-fast hot module replacement (HMR) and a highly optimized development experience.
*   **Basic HTML Structure:** A clean `index.html` to build upon.
*   **CSS Styling:** Integrated `src/style.css` for global styling, ready for your CSS experiments.
*   **JavaScript Interactivity:** Includes a simple counter example (`src/counter.js`) to demonstrate basic DOM manipulation.
*   **Asset Handling:** Demonstrates how Vite handles static assets like SVG images.

## Tech Stack

*   **Languages:**
    *   HTML5
    *   CSS3
    *   JavaScript (ES Modules)
*   **Build Tool / Development Server:**
    *   [Vite](https://vitejs.dev/) - A next-generation frontend tooling that provides an extremely fast development experience.
*   **Package Manager:**
    *   Bun (as indicated by `bun.lock`)
    *   npm / Yarn (also compatible)

## Architecture

This project follows a standard, flat structure typical for a small Vite application:

```
├── .gitignore
├── bun.lock
├── index.html                  # Main entry point for the web application
├── package.json                # Project metadata and dependencies
├── public/                     # Static assets served directly (e.g., vite.svg)
│   └── vite.svg
└── src/                        # Source code for the application
    ├── counter.js              # JavaScript module for the interactive counter
    ├── javascript.svg          # JavaScript logo asset
    ├── main.js                 # Main JavaScript entry point, imports CSS and other modules
    └── style.css               # Global CSS styles
```

**Key Components:**

*   **`index.html`**: The single page application's entry point. It loads `src/main.js`.
*   **`src/main.js`**: The primary JavaScript file that imports CSS, images, and other JavaScript modules (`counter.js`), then renders the initial HTML content into the `#app` div.
*   **`src/style.css`**: Contains the global styles for the application.
*   **`src/counter.js`**: A self-contained module responsible for setting up and managing the interactive counter button.

## Getting Started

Follow these steps to get your development environment up and running.

### Prerequisites

Before you begin, ensure you have the following installed:

*   **Node.js**: Version 18.x or higher.
    *   [Download Node.js](https://nodejs.org/en/download/)
*   **Bun** (recommended) or **npm** / **Yarn**: A package manager for installing dependencies.
    *   [Install Bun](https://bun.sh/docs/installation)
    *   [Install npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) (comes with Node.js)

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/onethenew/Learn-CSS.git
    cd Learn-CSS
    ```

2.  **Install dependencies:**
    Using Bun (recommended):
    ```bash
    bun install
    ```
    Or using npm:
    ```bash
    npm install
    ```

### Configuration

This project requires no specific environment variables or configuration files to get started. All configurations are handled by Vite's default settings and `package.json` scripts.

## Usage

### Running the Development Server

To start the development server with hot module replacement:

```bash
bun run dev
# or
npm run dev
```

This will typically open the application in your browser at `http://localhost:5173/`. You can now make changes to `index.html`, `src/style.css`, `src/main.js`, or `src/counter.js`, and the browser will automatically refresh to show your updates.

### Interacting with the Application

*   **Counter:** Click the button labeled "count is X" to increment the counter.
*   **Logos:** Click the Vite or JavaScript logos to visit their respective documentation pages.

### Building for Production

To create a production-ready build of the application:

```bash
bun run build
# or
npm run build
```

This command will compile and optimize your project files into the `dist/` directory, ready for deployment.

### Previewing the Production Build

You can locally preview the production build to ensure everything works as expected:

```bash
bun run preview
# or
npm run preview
```

This will serve the contents of the `dist/` directory.

## Development

### Setting Up Your Development Environment

Simply run `bun run dev` (or `npm run dev`) after installation. Your preferred code editor (e.g., VS Code) will automatically detect the project type.

### Code Structure

*   **`index.html`**: Modify this file to change the main structure of your application.
*   **`src/style.css`**: Add or modify CSS rules here to style your application.
*   **`src/main.js`**: This is where you can add global JavaScript logic, import components, or initialize your application.
*   **`src/counter.js`**: Examine this file to understand how a simple interactive component is created and exported.

### Code Style Guidelines

While no formal linter is configured, please adhere to standard JavaScript, HTML, and CSS best practices:

*   Use consistent indentation (2 spaces recommended).
*   Use meaningful variable and function names.
*   Keep functions small and focused.

## Deployment

To deploy this application, you will typically serve the contents of the `dist/` directory generated by `bun run build`.

1.  **Build the project:**
    ```bash
    bun run build
    ```
2.  **Deploy the `dist/` folder:**
    The `dist/` folder contains all the static assets (HTML, CSS, JS, images) needed to run your application. You can deploy this folder to any static site hosting service, such as:
    *   Netlify
    *   Vercel
    *   GitHub Pages
    *   Firebase Hosting
    *   Amazon S3 / CloudFront

## Contributing

Contributions are welcome! If you'd like to improve this learning project or fix an issue, please follow these steps:

1.  **Fork** the repository.
2.  **Create a new branch** for your feature or bug fix:
    ```bash
    git checkout -b feature/your-feature-name
    # or
    git checkout -b bugfix/issue-description
    ```
3.  **Make your changes** and commit them with clear, descriptive messages.
4.  **Push your branch** to your forked repository.
5.  **Open a Pull Request** to the `main` branch of this repository.

Please ensure your code adheres to the existing style and passes any local checks.

## Troubleshooting

*   **`Error: Cannot find module 'vite'`**: This usually means dependencies are not installed. Run `bun install` or `npm install`.
*   **Port already in use**: If `bun run dev` fails because the port is in use, you can either stop the process using that port or configure Vite to use a different port in `vite.config.js` (if you create one).
*   **Browser not refreshing**: Ensure your browser's developer tools are not blocking HMR, and check the console for any JavaScript errors.

## Roadmap

This project is primarily a learning sandbox, but future enhancements could include:

*   More complex CSS examples (e.g., animations, responsive design).
*   Integration of a simple JavaScript framework (e.g., React, Vue).
*   Introduction to state management.
*   Adding unit tests for JavaScript functions.

## License & Credits

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Credits:**

*   Built with [Vite](https://vitejs.dev/)
*   Powered by [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
*   Initial setup inspired by Vite's default templates.