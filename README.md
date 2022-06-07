# nodered-mqtt

Node-RED and Mosquitto deploy with flows

### Usage

```
git clone --recursive https://github.com/afreisinger/mqtt-nodered.git
docker-compose -up -d --buid
```

### Flow suggestion

1. Use the inject node wired to mqtt input to trigger messages
2. Use the debug node to log mqtt output messages.

### Cleanup
`docker-compose down` - will remove the containers and images


### Destroy
```
docker stop $(docker ps -a -q)                                                                                                                                                                                                                  190.245.120.45  22:40:54 | 5/06/22 ─╯
docker rm $(docker ps -a -q)
docker volume prune
```


* * *

### References

* https://github.com/node-red/cookbook.nodered.org/wiki/Connect-to-an-MQTT-broker
* https://github.com/node-red/cookbook.nodered.org/wiki/MQTT-Basics
* https://github.com/node-red/cookbook.nodered.org/wiki/How-to-safely-expose-Node-RED-to-the-Internet

* * *

### Example

### How to use the examples

Most examples can be triggered by clicking the button (left) tab on the inject nodes.
    * simple mqtt
    * multi in / one out mqtt
    * multi in / out mqtt

### Be careful with topics

While creating these examples I had to make sure that each flows topics were unique.

If the other flows were using the same topic, and those flows were enabled, they would also be listening for and processing the published messages.

That is why if you look at some of the nodes, you will see that one flows topics start with __example1/...__, then the next starts with __example2/...__ etc.

* * *

