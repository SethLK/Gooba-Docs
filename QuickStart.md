# Quick Start

## Project Structure

After generating a new project using GooBa, you will find the following directory structure:

    <project_name>/
	    output/
	    main.py
	    run.py
	    server.py
### Directory and Files

-   **`<project_name>/`**: The root directory of your project.
-   **`output/`**: A directory where the generated files will be stored.
-   **`main.py`**: The main script that creates a new HTML document using GooBa.
-   **`run.py`**: A script for starting the development server and watching for file changes.
-   **`server.py`**: A simple HTTP server script to serve your generated files.
## Getting Started

To start working with your new project, follow these steps:

1.  **Navigate to Your Project Directory**:
    
   Open a terminal or command prompt and navigate to your project directory:
   
    cd <project_name>


2.  **Run the Development Server**:

To start the development server and begin working on your project, execute the following command:

    python run.py

 This will start a development server on port 8000 and watch for any changes in your project files. The server will automatically restart when changes are detected.
    
3.  **Run the Development Server**::
    
    Open your web browser and navigate to `http://localhost:8000` to view your project.
    
### File Descriptions

 `main.py`

This file contains the main script that uses GooBa to create an HTML document. It sets up the document structure and generates the final HTML file.

 `run.py`

This script starts the development server and uses `watchdog` to monitor file changes. It will automatically restart the server whenever a change is detected.

 `server.py`

A simple HTTP server script that serves the generated files from the `output` directory. This script handles requests and provides the necessary files to the browser.

[Installation](Installation.md)
[How Gooba Work](HowGoobaInterpretsCode.md)
