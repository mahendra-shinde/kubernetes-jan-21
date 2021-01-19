DOCKER RUN 


docker run [OPTIONS] IMAGE-NAME [COMMAND/PROGRAM]

Options:
  -t (default)          Container would have OUTPUT terminal but accept no input
  -it                   Container would have I/O Terminal
                        The Command MUST be present after IMAGE-NAME
  -d, --detached        Container would have NO Terminal and takes NO input
                        Container would run in background.
  --name NAME           Provide User-defined name for container.
  -e  NAME=Value        Pass Name=Value pair as environment variable
  -p HostPort:GuestPort Port Forwarding between container and host system.
  -v HostPath:GuestPath Volume mounting (Mounting host directory inside container )  


