# Kubernetes Networking

Challenges:

- Where to run -> k8s includes a scheduler to pick nodes
- how to communicate with each other -> ensures communication in face of changes
- scaling the service -> has constructs to support scaling
- handling failure -> monitors and can restart containers

## Use

You can use [kind](https://kind.sigs.k8s.io/) for local testing on a single host
(k8s in docker).

`kubectl` is the management utility for controlling clusters. `.kube/config`
tells the utility to send API calls to the control plane container.

## Architecture
## Networking
## Creating a networking plugin
