# Predictive Maintenance Dashboard

An AI-powered predictive maintenance dashboard designed to monitor equipment health, analyze sensor data, detect anomalies, and support maintenance planning.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react\&logoColor=white)
![Python](https://img.shields.io/badge/Python-FastAPI-009688?logo=python\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?logo=postgresql\&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-scikit--learn-F7931E?logo=scikitlearn\&logoColor=white)

## Overview

The Predictive Maintenance Dashboard is a full-stack application designed to help users understand equipment conditions and make data-driven maintenance decisions.

The application combines a React frontend, a Python FastAPI backend, PostgreSQL database integration, and machine learning models to analyze equipment data. It is designed to estimate the time remaining before maintenance is required and identify unusual sensor patterns that may indicate potential equipment problems.

The project also includes configuration for containerization, automated testing, and deployment workflows.

## Features

* **Equipment Health Monitoring:** View equipment status and condition information through a centralized dashboard.
* **Predictive Maintenance:** Use a Random Forest regression model to estimate the time remaining before maintenance.
* **Anomaly Detection:** Apply an Isolation Forest model to identify unusual equipment sensor patterns.
* **Interactive Dashboard:** Visualize equipment information, sensor trends, and maintenance-related data.
* **Maintenance Tracking:** Record and review equipment maintenance activities.
* **AI-Powered Insights:** Integrate the Anthropic API to generate natural-language maintenance recommendations when configured.
* **Database Integration:** Use PostgreSQL for persistent application data.
* **REST API:** Connect the frontend and backend through FastAPI endpoints.
* **Containerization:** Use Docker and Docker Compose for supported development and deployment workflows.
* **Automated Testing and CI/CD:** Includes configuration for backend and frontend testing and automated build or deployment workflows.

## Tech Stack

| Category            | Technologies                                  |
| ------------------- | --------------------------------------------- |
| Frontend            | React, JavaScript, Recharts                   |
| Backend             | Python, FastAPI                               |
| Database            | PostgreSQL, SQLAlchemy                        |
| Machine Learning    | scikit-learn, Random Forest, Isolation Forest |
| AI Integration      | Anthropic API                                 |
| API Development     | REST APIs, Pydantic                           |
| Testing             | Pytest, Jest, React Testing Library           |
| Containerization    | Docker, Docker Compose                        |
| CI/CD               | GitHub Actions                                |
| Cloud Configuration | AWS-related deployment configuration          |

## Architecture

The application follows a full-stack architecture:

1. **Frontend:** React provides the dashboard interface and visualizations.
2. **Backend:** FastAPI handles application requests and backend processing.
3. **Database:** PostgreSQL stores application data.
4. **Machine Learning:** scikit-learn models support maintenance-time estimation and anomaly detection.
5. **AI Integration:** The Anthropic API can provide natural-language insights when correctly configured.
6. **Automation:** Docker and GitHub Actions configuration support containerized development and automated workflows.

## Repository Structure

The project contains frontend, backend, API, configuration, and deployment-related files.

```text
Predictive-Maintenance-Dashboard/
├── .github/
├── api/
├── backend/
├── docker/
├── infrastructure/
├── public/
├── src/
├── .dockerignore
├── .gitignore
├── Dockerfile.railway
├── docker-compose.yml
├── package.json
├── package-lock.json
├── README.md
├── railway.json
└── vercel.json
```

The exact structure may change as the project evolves.

## Getting Started

### Prerequisites

Install the following tools as required by the project configuration:

* Git
* Python
* Node.js and npm
* PostgreSQL or Docker
* Docker Compose, if using the provided container configuration

### 1. Clone the Repository

```bash
git clone https://github.com/heshmasree2809/Predictive-Maintenance-Dashboard.git
cd Predictive-Maintenance-Dashboard
```

### 2. Configure Environment Variables

Review the available `.env.example` files and identify the variables required by the frontend and backend.

Create the appropriate local environment files and configure your database connection and any required API keys.

**Security note:** Never commit real API keys, database passwords, access tokens, or production secrets to GitHub.

### 3. Start with Docker Compose

If the Docker Compose configuration is ready for your environment, run:

```bash
docker compose up --build
```

Check `docker-compose.yml` to confirm which services and ports are configured.

To stop the containers, run:

```bash
docker compose down
```

### 4. Run the Backend

Review the backend requirements and application entry point before running the following commands.

```bash
cd backend
python -m venv venv
```

On Windows:

```cmd
venv\Scripts\activate
```

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

If the backend entry point is `app.main:app`, start the API using:

```bash
uvicorn app.main:app --reload --port 8000
```

If available, the FastAPI interactive documentation can be accessed at:

```text
http://localhost:8000/docs
```

### 5. Run the Frontend

Open a separate terminal in the project root and install the frontend dependencies:

```bash
npm install
```

Start the frontend using the script defined in `package.json`. For a Create React App project, the command is:

```bash
npm start
```

Check `package.json` if the project uses a different development command.

## Testing

The repository includes configuration referring to backend and frontend automated tests.

For Python tests, if Pytest is installed and tests are configured:

```bash
python -m pytest
```

For frontend tests, use the test script defined in `package.json`. For a Jest-based Create React App project, this may be:

```bash
npm test -- --watchAll=false
```

Run these commands in the appropriate directories and verify the results. Test coverage and passing-test counts should be documented only after the test suites have actually been executed.

## Machine Learning

The project documentation describes two machine learning approaches:

### Random Forest Regression

Designed to estimate the remaining time before equipment maintenance is required using equipment-related input data.

### Isolation Forest

Designed to identify unusual patterns in sensor readings that may indicate abnormal equipment behavior.

Model performance should be evaluated using an appropriate dataset and documented metrics. For regression, possible metrics include Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE). For anomaly detection, precision and recall can be used when reliable labels are available.

No accuracy or performance figures are claimed here because verified evaluation results have not been provided.

## CI/CD and Deployment

The repository contains GitHub Actions and deployment-related configuration.

Review the workflow files in `.github/workflows/` to understand which tests, builds, and deployment steps are configured.

The project also contains configuration related to Docker, Railway, Vercel, and AWS infrastructure. The presence of these files does not, by itself, confirm that the application has been successfully deployed.

Add a live demo URL, deployment badge, or cloud architecture details only after verifying the corresponding deployment.

## Future Improvements

Potential improvements include:

* Evaluate machine learning models using a documented validation dataset.
* Add more equipment sensor datasets and improve data preprocessing.
* Expand automated tests for API endpoints and frontend components.
* Record model evaluation metrics and test results.
* Add screenshots of the running application.
* Verify and document a live cloud deployment.
* Improve monitoring, logging, and error handling.

## Author

**Heshma Sree Avuthu**

GitHub: [heshmasree2809](https://github.com/heshmasree2809)

## License

Refer to the repository's `LICENSE` file for the applicable license terms.
