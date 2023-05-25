# Example Kubernetes Application

This is an example Python application that checks the status and response time of a website and sends a message to a Discord channel using a webhook. The application is containerized using Docker and can be deployed on a Kubernetes cluster.

## Prerequisites

- Docker
- Kubernetes
- kubectl

## Getting Started

1. Clone this repository to your local machine.

```
git clone https://github.com/matthee500/example-kubernetes-application.git
```

2. Build the Docker image.

```
cd example-kubernetes-application
docker build -t localhost:5000/examplekubernetesapplication:0.2 .
```

3. Push the Docker image to your local registry.

```
docker push localhost:5000/examplekubernetesapplication:0.2
```

4. Deploy the application on your Kubernetes cluster.

```
kubectl apply -f deployment.yaml
```

5. Check the status of your deployment.

```
kubectl get deployments
```

## Usage

The application will check the status and response time of the websites specified in the `URL` environment variable of each container every 30 minutes and send a message to the Discord channel specified in the `discord_url` variable in `main.py`.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.