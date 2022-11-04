# stock-predictor
Build a basic time series model to predict stock prices and Deploy using FastAPI to AWS EC2

# Test the model
- In order to predict using the model use the command below:

curl \
--header "Content-Type: application/json" \
--request POST \
--data '{"ticker":"MSFT", "days":7}' \
http://18.206.223.225:8000/predict