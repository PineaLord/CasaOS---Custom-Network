# This command creates a custom Docker network with the correct label so that CasaOS Compose recognizes it. This prevents network label errors when attaching other containers to the network.

### Raw form

sudo docker network create --label com.docker.compose.network=***custom_network_name*** **custom_network_name**

```
sudo docker network create \
  --driver=bridge \
  --label com.docker.compose.network="custom_network" \
  "custom_network"

```

you can add follow if portainer not accept fix IP
```
 --subnet=172.22.0.0/16 \
  --gateway=172.22.0.1 \
```
