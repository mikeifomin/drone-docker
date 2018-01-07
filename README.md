# Better solution. without this plugin:

```yaml
deploy:
  privileged: true
  image: docker:17.10.0-dind
  volumes:
    - /var/run/docker.sock:/var/run/docker.sock
  commands:
    - "docker service update --image repo/image:${DRONE_TAG} service_name"
```

[link](https://discourse.drone.io/t/update-swarm-service-in-publish-pipeline/191/3)

