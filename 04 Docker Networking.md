# Docker Networking

Docker allows you to connect containers to each other and to the outside world through networking. In this guide, we'll explore the different types of Docker networking and how to use them.

## Types of Docker networking

### Bridge networking

By default, Docker creates a virtual network named `bridge` that allows containers to communicate with each other and the host machine. Containers can also be exposed to the outside world by mapping container ports to host ports.

### Host networking

With host networking, the container shares the same network stack as the host machine, allowing it to bypass the virtual network created by Docker. This can provide better performance, but it also means that the container shares the same IP address as the host machine.

### Overlay networking

Overlay networking allows containers to communicate with each other across multiple Docker hosts. This is useful for creating distributed applications that span multiple machines.

### Macvlan networking

With Macvlan networking, each container is assigned a unique MAC address and IP address on the host network. This allows the container to appear as a physical device on the network, which can be useful for certain types of applications.

## Using Docker networking

To use Docker networking, you can specify the network mode when creating a container:

```
docker run --network <NETWORK_NAME> <IMAGE_NAME>
```

You can also use the `docker network` command to create and manage Docker networks:

```
docker network create <NETWORK_NAME>
```

You can connect containers to a network using the `docker network connect` command:

```
docker network connect <NETWORK_NAME> <CONTAINER_NAME>
```

And you can disconnect containers from a network using the `docker network disconnect` command:

```
docker network disconnect <NETWORK_NAME> <CONTAINER_NAME>
```

## Conclusion

Docker networking is a powerful feature that allows you to create flexible and scalable applications. By understanding the different types of Docker networking and how to use them, you can take full advantage of Docker's capabilities.