# Deployment
This repository contains the code for the running the entire system using Docker Compose. The system consists of the following components:
- **Frontend:** UI for displaying the stress predictions.
- **Data Generator:** Generates mock physiological data.
- **Stress Predictor:** Performs stress predictions on the physiological data.
- **InfluxDB database:** Stores the mock physiological data and the predictions made by the stress predictor.
- **API:** Handles the communication between all of the services and the database.

To run the system, the repositories must first be cloned for the `frontend`, `data_generator`, `stress_predictor`, and `api` components. After cloning, ensure that all these repositories are placed within the same folder.

Next, a `.env` file must be created in the project root directory and it should be populated with the following environment variables:
```
INFLUX_USERNAME="USERNAME"
INFLUX_PASSWORD="PASSWORD"
INFLUX_BUCKET="BUCKET"
INFLUX_ORG="ORG"
INFLUX_TOKEN="TOKEN"
INFLUX_URL="http://influxdb:8086"
VITE_API_URL="http://api:3000"
API_URL="http://api:3000"
```
Ensure to replace `"USERNAME"`, `"PASSWORD"`, `"BUCKET"`, `"ORG"`, and `"TOKEN"` with your actual InfluxDB credentials and server information.

Then, run the following command in the terminal:
```
docker-compose up
```

## License
This project is licensed under the MIT License.