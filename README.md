# kubernetes-traefik-docker-nodejs-playground
Playing with Kubernetes, Traefik and Docker (running simple nodejs apps)

Arch:
- Kubernetes cluster
- Express app1 (2 replicas)
- Express app2 (3 replicas)
- Traefik (in front of both apps, serving as reverse proxy)

Goal:
- Be able to increase/decrease the number of replicas
- Be able to reach different apps by going to different sub-domains
- Add letsencrypt to Traefik
- Monitor everything
- Stress tests on both apps to check the auto management feature

All tests will be done on Ubuntu 18.04.3 LTS.

Notes:
- Test namespaces (kindof isolate both apps)
- Try to reduce the docker image as much as possible (eg: alpine, multistage builds)