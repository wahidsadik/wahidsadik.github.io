---
layout: post
title:  "Patterns with docker"
categories: architechture
tags: [architechture, docker, kubernetes]
---

I've been actively using Docker and Kubernetes (k8s) at work for a while now. Here are few patterns I gathered.

<!--more-->

# Patterns

## Docker

- docker-compose is quite handy to get started with brand-new projects.
- Use a repository. You can use [Gitlab Docker Registry](https://docs.gitlab.com/ee/user/project/container_registry.html), [portus](http://port.us.org/), etc.
- Master docker commandline.

## Kubernetes

- Use `minikube` locally to have a flavor of kubernetes.
- [helm chart](https://helm.sh/) is quite useful to roll-forward/roll-back containers.
