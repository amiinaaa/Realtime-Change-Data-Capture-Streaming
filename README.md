
# Realtime Change Data Capture (CDC) Streaming

## Project Overview

This project explores the concept of **Change Data Capture (CDC)** and implements it for real-time streaming of data changes. Using **Debezium** to track and capture data changes in a PostgreSQL database, the changes are streamed into **Kafka** topics in real-time. The project also includes the visualization of captured data and the events generated by Kafka, along with user information who made the changes and timestamps of the modifications.

## Features

- **Change Data Capture (CDC):** Implemented to track and capture changes in real-time from a PostgreSQL database.
- **Real-time Streaming:** Streams captured data changes into Kafka topics using Debezium connectors.
- **User Data Retrieval:** Retrieves detailed information about the user who modified the data along with timestamps for each change.
- **Data Visualization:** Visualizes the captured data and events flowing through Kafka.

## Technologies Used

- **Docker:** For containerization of all components in the architecture.
- **PostgreSQL:** Database used to demonstrate change capture.
- **Debezium:** A distributed platform for CDC to stream database changes.
- **Kafka:** Message broker for streaming the data changes.

## Getting Started

### Prerequisites

Ensure that you have the following tools installed:
- Docker
- Docker Compose
- Kafka CLI (optional, for manual topic monitoring)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/amiinaaa/realtime-cdc-streaming.git
   cd realtime-cdc-streaming
   ```

2. **Start the environment:**

   Use Docker Compose to spin up the required containers for PostgreSQL, Kafka, and Debezium:

   ```bash
   docker-compose up
   ```

3. **Set up the PostgreSQL database:**

   Once the environment is up and running, populate the PostgreSQL database with initial data.

4. **Configure Debezium:**

   Set up a Debezium connector to monitor the PostgreSQL database for any changes. The changes will automatically stream into the appropriate Kafka topics.

### Usage

- **Monitor data changes:** Any updates, inserts, or deletes in the PostgreSQL database will be captured and streamed in real-time.
- **View captured data:** You can view the captured changes in Kafka topics through a Kafka consumer or visualization tool of your choice.
  
### Visualizing Events

You can use any Kafka-compatible visualization tool to monitor the flow of CDC events in real-time.

### Example

When a user modifies data in the PostgreSQL database, Debezium captures the event and streams it into Kafka. You can retrieve the event, including:
- The modified data.
- Information about the user who performed the modification.
- The timestamp when the modification occurred.

## License

This project is licensed under the MIT License.
