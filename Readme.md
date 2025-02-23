﻿# receipt-process
This project implements a web service to process receipts and calculate points according to predefined rules. It is built with Java (Spring Boot) and can be easily run using Docker.

Prerequisites:
Java 17
Docker

Instructions to Build and Run with Docker
1. Build the Docker Image
  
   docker build -t receipt-processor .
2. Run the Docker Container
  
   docker run -p 8080:8080 receipt-processor
3. Test the API
   Use curl or Postman to interact with the API:

Submit a Receipt:
Example:
curl -X POST http://localhost:8080/receipts/process \
-H "Content-Type: application/json" \
-d '{"retailer":"Target","purchaseDate":"2022-01-01","purchaseTime":"13:01","items":[{"shortDescription":"Item1","price":"5.00"}],"total":"5.00"}'

Retrieve Points:

curl http://localhost:8080/receipts/{id}/points

