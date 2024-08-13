# Docker ELK

Module: **Virtualization** </br>
Competency: [is able to use Docker to containerize applications](./evaluation.md) </br>
Duration: **5 days** </br>
Participant(s): **solo** </br>
Output: **comment on issue**

## The mission

Unleash the power of **simple portability** through **process isolation** with Docker! In this challenge, you'll explore `docker` and `docker-compose` to containerize and deploy the **ELK Stack (Elasticsearch, Kibana, Beats, and Logstash)** locally.

### Follow the Instructions:

1. **Install and Explore:**
    * Get `docker` on your machine.
    * Master the Docker CLI and Dockerfiles: [https://labs.play-with-docker.com/](https://labs.play-with-docker.com/)
    * Install `docker-compose` and conquer its secrets: [https://takacsmark.com/docker-compose-tutorial-beginners-by-example-basics/](https://takacsmark.com/docker-compose-tutorial-beginners-by-example-basics/)

2. **Containerize Individually:**
    * Choose a Beat (like Filebeat) to containerize.
    * Craft a Dockerfile capturing its installation and configuration.
    * Run the container and ensure it works.
    * Repeat for other Beats and Logstash (optional).
    * Explore official Docker images for Elasticsearch and Kibana:
        * Elasticsearch: [https://hub.docker.com/_/elasticsearch/](https://hub.docker.com/_/elasticsearch/)
        * Kibana: [https://hub.docker.com/_/kibana/](https://hub.docker.com/_/kibana/)

3. **Build the ELK Stack:**
    * Create a `docker-compose.yml` file:
        * Define services for Elasticsearch, Kibana, Beats/Logstash (with volumes and ports).
        * Configure network connections for container communication.
    * Build and launch the stack using `docker-compose up -d`.

4. **Explore and Analyze:**
    * Access the Kibana UI (usually at http://localhost:5601).
    * Configure data ingestion from your chosen Beat (e.g., logs from a local file).
    * Dive into your data with Kibana dashboards and visualizations.

5. **Bonus Challenge:**
    * Build data pipelines with Logstash for advanced filtering and processing.
    * Connect to external data sources (like databases) for broader monitoring.

**Remember:**

* Monitor containers with `docker ps`, `docker logs`, and `docker-compose logs`.
* For detailed configuration options, refer to official docs:
    * [Beats]()
    * [Logstash]()
    * [Elasticsearch]()
    * [Kibana]()

**Output:**

* Share your experience, challenges, and learnings on the challenge issue.
* Include your `docker-compose.yml` file and any cool visualizations you created.

**Good luck!**

**Note:** This focuses on core ELK Stack functionality. Feel free to explore further customization and advanced features.

**Example Docker Compose File for Filebeat:**

```yaml
version: "3.8"

services:
  filebeat:
    image: elastic/filebeat:latest
    volumes:
      - ./filebeat.yml:/etc/filebeat/filebeat.yml:ro
      - ./logs:/var/log/filebeat
    environment:
      FILEBEAT_INPUTS: - type: log paths: ["/var/log/*"]
    restart: unless-stopped

networks:
  elk:

# Replace other services with similar structure based on their configurations
```

## Complementary Resources

* Tuto: [Create your own image](https://docs.docker.com/develop/develop-images/baseimages/)
* Doc: [Docker documentation](https://docs.docker.com/)
* Doc: [Docker Compose documentation](https://docs.docker.com/compose/)


![Briefing's GIF](https://c.tenor.com/z3Vqx6hmE5QAAAAC/whale-docker.gif)
