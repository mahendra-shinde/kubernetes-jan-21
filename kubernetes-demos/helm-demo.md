# Helm : Package Manager

1. Managed Kubernetes deployments
2. Allows to package all kubernetes API objects into single "Charts"
3. Allows Sharing charts with other members using "repos"

## Install Helm

1. Download the binary from https://github.com/helm/helm/releases
2. Extract the contents in local disk and set PATH variable to point this location

    ex: On My Machine, "helm.exe" is inside "C:\helm" directory and its in PATH vars

3. Add an existing PUBLIC HELM REPO (bitnami)

    ```
    $ helm repo add bitnami https://charts.bitnami.com/bitnami
    $ helm repo update
    ```

4.  Download a "chart" and extract in local folder

    ```
    $ helm search repo mongo
    ## Download in current directory
    $  helm pull bitnami/mongodb --untar
    ```

5.  To install local chart

    ```
    $ helm install  mymongo .\mongodb
    ### OR
    $ helm install mymongo bitnami\mongodb
    ```

6.  List all helm deployments

    ```
    $ helm list
    ```

7.  Uninstall a chart

    ```
    $ helm uninstall mymongo
    ```