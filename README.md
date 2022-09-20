# bicep-extensibility-node
Test repo for publishing a NodeJS webapp container with the Bicep extensibility protocol

## Running locally
1. Open in Codespaces
1. Build: 
    ```sh
    docker build -t extserver:latest ./
    ```
1. Run: 
    ```sh
    docker run -p 8080:8080 extserver:latest
    ```
1. Test locally:
    ```sh
    curl -X POST http://localhost:8080/Save \
      -H 'Content-Type: application/json' \
      -d '{"import":{"provider":"foo","version":"1.0","config":{}},"resource":{"type":"bar@v1","properties":{}}}'