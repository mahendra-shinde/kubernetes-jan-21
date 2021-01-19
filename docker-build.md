# Docker Build

1.  Build a new user-defined container image from an existing BASE image or USER-defined image.
2.  Docker build requires a proper directory structure

    project-directory/
      -- Dockerfile (mandatory, and Case-Sensitive)
      -- .dockerignore (optional, skip few files from build)
      -- Application Source or Binaries
      -- Application Dependencies / Build Script

3.  Syntax of Docker build

    ```
    $ docker build -t NEW-IMAGENAME [--no-cache] [PROJECT-DIRECTORY]
    # Example
    $ docker build -t phpapp .
    $ docker build -t phpapp c:\demos\php-app
    ```

4.  Second build would use "Build Cache" created by FIRST build.
5.  But, If any changes are detected, then CACHE is skipped.
