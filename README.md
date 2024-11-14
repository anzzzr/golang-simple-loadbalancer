# Simple GoLang Load Balancer

This is a simple load balancer implemented in GoLang designed to distribute incoming network traffic across multiple servers. It helps optimize resource usage, improves response times, and prevents overload on individual servers.

## Features

- **Round-robin Load Balancing**: Distributes traffic evenly across multiple backend servers.
- **Concurrency**: Utilizes GoLang's goroutines to handle multiple requests concurrently for better performance.
- **Customizable**: Easily add or remove backend servers to suit the needs of your application.
- **Basic Monitoring**: Supports basic server health checks to ensure requests are routed to active servers.

## Requirements

- Go 1.16 or higher
- Linux-based environment (recommended for real-world deployment)
- Basic understanding of GoLang and networking concepts

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/simplelb.git
    cd simplelb
    ```

2. Build the project:
    ```bash
    go build -o loadbalancer main.go
    ```

3. Run the load balancer:
    ```bash
    ./loadbalancer
    ```

   You can configure the backend servers by editing the `servers` slice in the `main.go` file.

## Usage

- By default, the load balancer listens on port `8080` and distributes incoming HTTP requests to a predefined list of backend servers.
- You can add new backend servers by modifying the `backendServers` array in the `main.go` file.

## Example Configuration

```go
var backendServers = []string{
    "http://localhost:8001",
    "http://localhost:8002",
    "http://localhost:8003",
}
