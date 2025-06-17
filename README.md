# Golang Web Server Clean Architecture
## Family Guy Server

A web server built with Go, following clean architecture principles, designed to provide efficient and scalable APIs using GraphQL, gRPC, and REST, with data storage in ClickHouse and message streaming via Kafka.

## Technologies

This project leverages the following technologies:

- **[Go](https://golang.org/)**: The primary programming language for building the server.
- **[Gin](https://github.com/gin-gonic/gin)**: A high-performance HTTP web framework for Go.
- **[GraphQL](https://graphql.org/)**: For flexible and efficient API queries.
- **[gRPC](https://grpc.io/)**: For high-performance, type-safe remote procedure calls.
- **[Protobuf](https://protobuf.dev/)**: Protocol Buffers for defining gRPC service contracts and serialization.
- **[ClickHouse](https://clickhouse.com/)**: A high-performance columnar database for analytics.
- **[Kafka](https://kafka.apache.org/)**: A distributed streaming platform for handling real-time data.
- **[Testcontainers](https://testcontainers.org/)**: For integration testing without mocking databases or Kafka.
- **[Makefile](https://www.gnu.org/software/make/)**: For automating build and deployment tasks.

## Installation

To set up the project locally, ensure you have Go installed, then follow these steps:

1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd <repository-directory>
   Install dependencies:
   ```
```sh
go mod download
Start the server:
```
```sh

go run main.go
For production environments:
sh



GO_ENV=production go run main.go
Building for Production
To build the project for production:

sh



make build
To generate SQL files (e.g., for database migrations):

sh



make generate-sql
Docker
To build and run the project using Docker:

Build the Docker image:
sh



cd <repository-directory>
docker build -t <youruser>/family-guy-server .
Run the Docker container:
sh



docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=family-guy-server <youruser>/family-guy-server
Plugins
The project currently does not include additional plugins. Future plugins will be documented here with usage instructions.


TODOs
Implement remaining GraphQL API endpoints.
Optimize gRPC service performance.
Add more integration tests using Testcontainers.
Finalize ClickHouse schema design.
Configure Kafka topics and consumers.