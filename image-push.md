# Sharing container images

1.  DOCKER-CLI can have multiple persistent logins to docker registries.

    ```
    # Login into docker-hub
    $ docker login <ENTER>
    Username: 
    Password:
    ## Login into another registry (on-premise, acr, ecr)
    $ docker login registry-url
    Username: 
    Password: 
    ```

2.  Re-TAG your images to include "registry name" or "docker-hub username" (Use Powershell)

    ```
    $ $USERNAME="mahendrshinde"
    $ docker tag phpapp $USERNAME/phpapp
    $ docker push $USERNAME/phpapp
    ```

3.  Re-TAG your images to include "registry name" incase of hosted registry (ACR/ECR/GCR)

    ```
    $ $REGISTRY="az101.azurecr.io"
    $ docker tag phpapp $REGISTRY/phpapp
    $ docker push $REGISTRY/phpapp
    ```