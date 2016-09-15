# Private Docker Registry

This repository is a for testing private docker registry

Require docker and docker-compose

Default port is 5000

To start it:
```bash
docker-compose up -d
```

To test it
```bash
docker login http://localhost:5000
# default user:password test:test
docker pull ubuntu
docker tag ubuntu localhost:5000/ubuntu
docker push localhost:5000/ubuntu
```

... then pull it back from your registry:
```bash
docker pull localhost:5000/ubuntu
```

### References
* https://docs.docker.com/registry/deploying/
* https://docs.docker.com/registry/storage-drivers/s3/
