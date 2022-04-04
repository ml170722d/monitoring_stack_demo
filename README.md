# Monitoring stack Demo

This project is an introduction to monitoring stack.
Tools used for monitoring are Prometheus and Grafana.

### Requirements

* docker
* docker-compose

### How to start

1.  Run docker compose
    ```
        docker-compose up
    ```
    or
    ```
        docker-compose up -d
    ```
    in detacked mode to start the containers

2.  Open
    * Grafana http://localhost:3000/
    * Prometheus http://localhost:9090/

3.  To trigger the alerts in Prometheus find yak-server container name and stop it
    ```
        docker ps       # displays information about all running containers
        docker stop <container_name>
    ```
    After 1 min, Prometheus will start giving alerts that it can't scrape data from yak-server

