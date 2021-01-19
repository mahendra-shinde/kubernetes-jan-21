# Compose demo1

1. Create "docker-compose.yml" file in an empty folder. folder wont be empty after file is created :)
2. use following commands:

    ```
    # Validate the compose file
    $ docker-compose config
    # Create & Run all containers
    $ docker-compose up -d
    # check number of container inside current application
    $ docker-compose ps
    $ Check the processes inside containers
    $ docker-compose top
    # Logs for all container instance
    $ docker-compose logs -- app
    $ docker-compose down
    ```