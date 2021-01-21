# Docker Swarm

- Built in Container Orchestrator for Docker Runtime
- Easy Setup
  
   On Manager node:
    docker swarm init --advertise-addr [NODE-IP-ADDRESS]

   On Worker Node:
    docker swarm join --token [TOKEN-FROM-MANAGER] MANAGER-IP:PORT

- How to promote WORKER to MASTER? (Run from existing manager node)

    docker node promote worker-node

- How to demote MANAGER to WORKER (Run from existing manager node)

    docker node demote manager-node

- Any node, wants to leave ?

    docker swarm leave