# Create SAM apps (sample-sam)
sam init --runtime python3.9 --dependency-manager pip --app-template hello-world --name sample-sam

cd sample-sam

sam build

sam deploy --guided

curl API-ENDPOINT-URL