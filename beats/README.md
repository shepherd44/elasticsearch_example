# Metricbeat

## usage

* run

    ```script
    ELK_VERSION=7.14.2 docker-compose up -d
    ```

* stop

    ```script
    ELK_VERSION=7.14.2 docker-compose down
    ```

## index and dashboard setup

Running Metricbeat with the setup command will create the index pattern and load visualizations, dashboards, and machine learning jobs.

* metricbeat setup

    ```script
    docker run \
        --network elastic \
        docker.elastic.co/beats/metricbeat:7.14.2 \
        setup \
        -E setup.kibana.host=kibana:5601 \
        -E output.elasticsearch.hosts=["es:9200"]
    ```

* filebeat setup

    ```script
    docker run \
        --network elastic \
        docker.elastic.co/beats/filebeat:7.14.2 \
        setup \
        -E setup.kibana.host=kibana:5601 \
        -E output.elasticsearch.hosts=["es:9200"]
    ```
