# Docker network (Linux mode)

Driver Name | Description | Number of Networks supported
------------|-------------|-------------------------------
Null        | Disabled Networking | One network pre-created by Docker daemon, "none". You cannot create additinal networks from this driver.
Host        | Connects containers to HOST System network interfaces | One network pre-created by docker daemon, "Host". You cannot create any addition Host networks.
Bridge     | Allows creation of metworks with different IP Address ranges. | One network pre-created by Docker daemon, "bridge". Any number of additional networks can be created. Just avoid overlapping IP Addresses.