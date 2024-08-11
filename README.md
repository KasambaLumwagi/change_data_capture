# Change Data Capture (CDC) Data Engineering Project

## Table of Contents

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Architecture](#architecture)
4. [Setup and Configuration](#setup-and-configuration)
5. [Steps to Run the Project](#steps-to-run-the-project)
6. [Best Practices](#best-practices)
7. [Contribution](#contribution)
8. [License](#license)

## Project Overview

This project demonstrates the implementation of a Change Data Capture (CDC) pipeline using Apache Kafka, Debezium, and PostgreSQL. CDC is a powerful technique for tracking and capturing data changes in real-time, allowing for the synchronization of data across different systems. The project showcases a complete CDC architecture, where data changes in a PostgreSQL database are captured and streamed through Kafka using Debezium.

## Technologies Used

- **Apache Kafka**: A distributed streaming platform used for building real-time data pipelines and streaming applications. Kafka is responsible for ingesting and streaming data changes.
- **Debezium**: An open-source distributed platform for change data capture, which tracks changes in your database and streams them to Kafka.
- **PostgreSQL**: A powerful, open-source object-relational database system used as the source database in this project. Changes in this database are captured using Debezium.
- **Kafka Control Center**: A web-based tool for managing and monitoring Kafka clusters, making it easier to oversee the data streams.
- **Debezium UI**: A web-based interface that allows you to manage and monitor Debezium connectors.
- **Docker**: Used to containerize the services and manage the deployment of the CDC stack.

## Architecture

The architecture of this project includes the following components:

- **Zookeeper**: Manages and coordinates Kafka brokers.
- **Kafka Broker**: Handles the ingestion and streaming of data.
- **Kafka Control Center**: Provides a web interface to monitor and manage the Kafka cluster.
- **Debezium**: Captures changes from the PostgreSQL database and streams them to Kafka.
- **Debezium UI**: A web interface for managing and monitoring Debezium connectors.
- **PostgreSQL**: The source database where changes are captured.

## Setup and Configuration

To set up the project, ensure that you have Docker and Docker Compose installed on your machine. The following steps outline the setup process:

1. **Clone the Repository**: Clone this repository to your local machine.

   ```bash
   git clone <repository_url>
   cd <project_directory>

## Docker Setup

2.The project uses Docker Compose to set up and run all the services. The services include:

- Zookeeper
- Kafka
- Kafka Control Center
- Debezium
- Debezium UI
- PostgreSQL

The `docker-compose.yml` file is pre-configured to run all these services in Docker containers.

## Environment Variables

Ensure that the necessary environment variables are set. These variables include configuration settings for Kafka, Debezium, and PostgreSQL. The variables are defined in the `docker-compose.yml` file.

## Service Health Checks

The Docker Compose setup includes health checks for each service, ensuring that all services are running correctly before other dependent services start.

## Steps to Run the Project

To get started with the project, follow these steps:

1. **Start the Services**: Use Docker Compose to start all the services.

   ```bash
   docker-compose up -d
