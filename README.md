# AI-Powered Web Scraper and Data Extraction Platform

<p align="center">
  <img src="https://img.shields.io/badge/Stack-AI%20%7C%20Web%20Scraping%20%7C%20Data%20Extraction-007bff?style=for-the-badge&logo=github&logoColor=white" alt="Tech Stack Badge" />
  <img src="https://img.shields.io/badge/Backend-Python%20%7C%20Flask-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Backend Badge" />
  <img src="https://img.shields.io/badge/AI-OpenAI%20%7C%20GPT--4o--mini-000000?style=for-the-badge&logo=openai&logoColor=white" alt="AI Badge" />
</p>

---

## Project Overview

The **Enhanced AI Web Scraper Pro** is a sophisticated, enterprise-grade web scraping application designed to extract structured data from websites with high accuracy and efficiency. This tool leverages a powerful combination of web automation, artificial intelligence, and a robust backend infrastructure to provide a seamless data extraction experience. The application is designed for scalability and monetization, offering a valuable service for businesses, researchers, and data analysts who require reliable and structured web data.

<div align="center">
  <p><a href="https://github.com/lewis-hue/AI-Powered-Web-Scraper-Data-Extraction-Platform/blob/main/Web%20Scraper%20Demo%20Video%20(2).mp4">🎬 Watch the Demo Video!</a> See the application in action and discover its powerful features.</p>
</div>

---

## Key Features

- **AI-Powered Data Extraction**: Utilizes OpenAI's GPT models to intelligently parse and structure data from unstructured HTML content.
- **Dynamic Content Handling**: Employs Playwright for robust scraping of dynamic, JavaScript-rendered websites.
- **Asynchronous Job Processing**: Manages scraping tasks in the background, allowing for a non-blocking user experience.
- **Real-time Job Monitoring**: Provides users with live updates on the status of their scraping jobs.
- **Multi-Page Scraping**: Capable of navigating through pagination to scrape data from multiple pages of a website.
- **Flexible Data Export**: Allows users to export scraped data in both CSV and XLSX formats.
- **Scalable Architecture**: Built with a modular design that can be scaled to handle a high volume of scraping requests.
- **Robust Error Handling**: Implements comprehensive error handling and retry mechanisms to ensure job reliability.

---

## Technical Stack

| Component        | Technology                              |
|------------------|-----------------------------------------|
| **Backend**      | Flask (Python)                          |
| **Frontend**     | HTML5, CSS3, JavaScript                 |
| **Web Scraping** | Playwright                               |
| **AI Processing**| OpenAI API (GPT-4o-mini)                |
| **Database**     | MongoDB                                 |
| **Data Handling**| Pandas                                  |
| **Deployment**   | Gunicorn/Waitress (Production Server)   |

---

## Architecture & Implementation

### 1. System Architecture and Design

- **Backend**: The backend is a **Flask-based monolithic application** designed for clarity and ease of development. It handles all core logic, including API requests, job queuing, web scraping, AI processing, and database interactions.
- **Frontend**: The frontend is a **single-page application (SPA)** built with standard web technologies. It provides a user-friendly interface for initiating and monitoring scraping jobs.
- **Database**: The application utilizes two main collections in MongoDB: `scraping_jobs` and `export_jobs`, which store information about scraping tasks and data export requests, respectively.

### 2. Data Extraction and Processing Pipeline

The data extraction process follows a multi-stage pipeline:

#### flowchart TD
---
    Stage 1: User Submission & Job Initiation
    A[👤 User Submits URL]
    B[💡 Job Initiation: 'pending']
    end

    Stage 2: Web Scraping & HTML Processing
    C{🌐 Background Thread<br/>(Playwright)}
    D[📝 Raw HTML Extraction]
    E[🧹 HTML-to-Markdown Cleaning]
    end

    Stage 3: Data Validation & Job Completion
    F{🧠 OpenAI API<br/>(Structured Data Extraction)}
    G[📦 Data Validation & Storage<br/>(MongoDB)]
    H[✅ Job Status: 'completed']
    end
    
    Stage 4: Error Handling
    I[🚧 Error Handling & Retries]
    end
---

## API and Endpoints

The application provides a set of RESTful API endpoints to manage scraping and export jobs.

## Available Endpoints

| Endpoint                          | Method | Description                                               |
| ---------------------------------- | ------ | --------------------------------------------------------- |
| `/scrape`                          | POST   | Initiates a new scraping job.                             |
| `/status/<job_id>`                 | GET    | Retrieves the status of a specific scraping job.          |
| `/export/<job_id>`                 | POST   | Creates a request to export data from a specific job.     |
| `/export-status/<export_job_id>`   | GET    | Checks the status of an export job.                       |
| `/download/<export_job_id>`        | GET    | Downloads the exported file associated with the export job.|

---

## Scalability and Performance

The application is designed with scalability in mind, featuring:

- **Asynchronous processing** to handle multiple tasks concurrently.
- **Horizontal scaling** of the Flask application to manage increased traffic.
- A **scalable MongoDB database** to ensure efficient data handling.

Future enhancements may include integrating a distributed task queue system, such as **Celery**, for improved performance and task management.

---

## Deployment and Monetization

### Deployment Strategy

The application follows a modern cloud deployment strategy utilizing:

- **Docker containers** for seamless environment setup and portability.
- **Managed cloud hosting services** (e.g., AWS, GCP, Heroku) for robust cloud infrastructure.
- **MongoDB Atlas** as a fully-managed database solution.
- A **CI/CD pipeline** for automated, continuous deployment.

### Monetization Model

A **freemium subscription model** is proposed for monetization:

- **Free tier**: Provides basic features with limited usage.
- **Premium tiers**:
  - **Pro**: Offers higher limits, advanced features, and API access.
  - **Business**: Includes all Pro features, with added benefits like dedicated support.
