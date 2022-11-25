# About the project
* The main purpose of this project is to build a basic time series model to predict stock prices and Build a container image for a FastAPI application

### Prerequisites

* Install Docker 
  

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/kedir/stock-predictor.git
   ```
2. Build the Docker Image
   ```sh
   docker build -t stock-prophet .
   ```
3. Verify the image has been built
   ```sh
   docker image -ls # docker images.
   ```
4. Start the container
   ```sh
   docker run -d --rm --name mycontainer -p 8000:8000 stock-prophet.
   ```
5. Verify the container is running
   ```sh
   docker ps -a.
   ```
6. Now the app should be running on port 8000 and you can run the prediction
   ```sh
    curl \
    --header "Content-Type: application/json" \
    --request POST \
    --data '{"ticker":"MSFT", "days":7}' \
    http://0.0.0.0:8000/predict   
   ```
