
# MLOps Flask Product Recommendation System

This project is a simple product recommendation system built using a Flask web application, a machine learning model based on **Singular Value Decomposition (SVD)**, and Docker for containerization. The system predicts product ratings for users based on historical interaction data.

## Features

- **Flask Web Application**: A web interface where users can select user IDs and product IDs to get product recommendations.
- **Machine Learning Model**: The recommendation model is trained using the `scikit-surprise` library with SVD for collaborative filtering.
- **Dockerized Application**: The app is fully containerized using Docker and can be deployed on any machine with Docker support.
- **Responsive Web Interface**: The web app is styled using Bootstrap for a clean and responsive design.
- **Modular Project Structure**: Cleanly separated logic for model loading, web interface, and prediction.

## Project Structure

```
MLOps_Flask_Recommendation_System/
├── app.py                 # Main Flask application
├── Dockerfile             # Dockerfile to containerize the Flask app
├── docker-compose.yml     # Docker Compose for managing the Docker container
├── requirements.txt       # Python dependencies for the project
├── model/
│   └── svd_model.pkl      # Trained SVD model
└── templates/
    ├── index.html         # HTML template for the form (input)
    └── result.html        # HTML template for displaying recommendation results
```

## Getting Started

### Prerequisites

- **Docker**: You need Docker installed to run the application.
- **Docker Compose**: Ensure Docker Compose is installed for easy container management.

### Running the Application

1. Clone the repository:

    ```bash
    git clone <repository-url>
    cd MLOps_Flask_Recommendation_System
    ```

2. Build and run the Docker container using Docker Compose:

    ```bash
    docker-compose up --build
    ```

3. Open your browser and go to `http://localhost:5000`.

4. Select a user ID and product ID from the dropdowns to get a product recommendation based on the trained model.

### Stopping the Application

To stop the running application, you can use:

```bash
docker-compose down
```

## Customization

- **Model**: You can retrain the model using the `scikit-surprise` library and replace the existing `svd_model.pkl` in the `model/` directory.
- **Data**: Modify or add new users and products by replacing the model training dataset.

## Future Enhancements

- Add a database (e.g., PostgreSQL) for storing user and product data.
- Implement continuous integration (CI) and continuous deployment (CD) pipelines using Jenkins or GitHub Actions.
- Deploy the application to a cloud platform like AWS, GCP, or Azure.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
