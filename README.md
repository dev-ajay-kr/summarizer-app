# PDF Summarizer with Gemini Pro

This project is a web application that summarizes the content of PDF files using Google's Gemini Pro model. Users can upload a PDF, provide a prompt, and receive a summary of the document.

## Features

*   **PDF Upload:** Upload PDF files through a simple web interface.
*   **Custom Prompts:** Provide custom instructions to guide the summarization process.
*   **Gemini Pro Integration:** Utilizes the power of Google's Gemini Pro model for high-quality text summarization.
*   **Web-Based Interface:** Easy-to-use interface for interacting with the application.

## Technology Stack

*   **Backend:** Flask
*   **Frontend:** HTML, CSS (Bootstrap)
*   **Language:** Python
*   **Google Cloud:**
    *   Vertex AI (for Gemini Pro)
*   **Libraries:**
    *   LangChain
    *   PyPDF
    *   Flask-WTF

## Prerequisites

*   Python 3.11
*   A Google Cloud project with the Vertex AI API enabled.
*   `gcloud` CLI authenticated to your Google Cloud project.
*   Docker (optional, for containerized deployment).

## Installation and Usage

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2.  **Set up a virtual environment and install dependencies:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```

3.  **Configure Google Cloud authentication:**

    Make sure you have the `gcloud` CLI installed and authenticated. Set your project ID as an environment variable:

    ```bash
    export PROJECT_ID="your-gcp-project-id"
    ```

4.  **Run the application:**

    ```bash
    python3 app.py
    ```

    The application will be available at `http://127.0.0.1:8080`.

## Deployment

This application is containerized using Docker. To deploy it, follow these steps:

1.  **Build the Docker image:**

    ```bash
    docker build -t pdf-summarizer .
    ```

2.  **Run the Docker container:**

    ```bash
    docker run -p 8080:8080 -e PROJECT_ID="your-gcp-project-id" pdf-summarizer
    ```

    The application will be available at `http://0.0.0.0:8080`.
