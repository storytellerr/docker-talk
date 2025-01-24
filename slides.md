---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /container.webp
# some information about your slides (markdown enabled)
title: Welcome to Containerization Talk
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Containerization

A Game Changer for Web App Deployments!

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Let's Dive into Containers 
</div>



<!-- ------------------------------------------------------------------------ -->

---
layout: center
transition: fade-out
---

# Why Containers required

<img border="rounded" src="/public/works.jpg" alt="" >





<!-- ------------------------------------------------------------------------ -->


---
class: px-20
---

# Hypervisor Vs Container

The key difference between Docker and a hypervisor lies in how they manage virtualization and the way they use system resources to isolate applications or environments.

<div grid="~ cols-2 gap-2" m="t-2">



```yaml
Heavier, more resource-intensive
Fully isolated, with its own OS
```

```yaml

Lightweight, less overhead
Shares the host OS kernel
```


<img border="rounded" src="/public/hypervisor1.png" alt="" >

<img border="rounded" src="/public/container.png" alt="" >

</div>
<div v-click>
Docker uses lightweight containers to share the <span v-mark.red="2">host OS kernel</span >, while hypervisors virtualize entire operating systems, making Docker more efficient and faster.
</div v-click>




<!-- ------------------------------------------------------------------------ -->
---
transition: fade-out
---

# Key Terms

- 📃 **Image**: standalone, executable package that includes everything needed to run
a piece of software (code, runtime libraries, configuration files). Provides the
filesystem and metadata (e.g. environment variables, initial working directory) for
a container.

- 📦 **Container**: a process isolated from the rest of the system through abstractions
created by the OS. The level of isolation can be controlled, allowing access to
host resources. Its filesystem content comes from an image.

<div style="display:flex; gap:100px">
  <div v-click>
    <img border="rounded" src="/public/image_run.png" alt="">
  </div>
  <div v-click>
    <img border="rounded" src="/public/image_layer.png" alt="" style="height:150px;">
  </div>
</div>



<!-- -------------------------------------------------------------------------------- -->

---
class: text-center
transition: fade-out
---

# Docker Image

We can run `Docker image ls` to see all images.
<div v-click>

This will show all images in machine:

<img border="rounded" src="/public/image_ls.png" alt="" >

</div>






<!-- -------------------------------------------------------------------------------- -->



---
class: text-center
transition: fade-out
---

# Docker Container

We can run `Docker container ls` to see all containers.
<div v-click>

This will show all **active** containers in machine:

<img border="rounded" src="/public/container_ls.png" alt="" >

</div>




<!-- -------------------------------------------------------------------------------- -->



---
class: text-center
transition: fade-out
---

# Build Ship Run(AnyWhere, AnyMachine)

The "Build, Ship, and Run" strategy in Docker involves creating a Docker image, distributing it via a registry, and then running the image as a container in any environment.

<img border="rounded" src="/public/build_ship_run.png" style="display: block; margin-left: auto; margin-right: auto;"  >

<div v-click>
Several remote registries available (e.g. <span v-mark.circle.orange="2">Docker Hub</span>, <span v-mark.circle.orange="3">GHCR</span>)

</div>

[Docker Hub](https://hub.docker.com/)

[Baatcheet GHCR](https://github.com/LatticeInnovations/baatcheet-frontend)


<!-- -------------------------------------------------------------------------------- -->



---
transition: fade-out
---

# Let's Create Our Own Image

- Choose a base Image
- Add or Upadate some data 
- Build image
- Push Image to repo.
- Run anywhere

<!-- -------------------------------------------------------------------------------- -->



---
transition: fade-out
---

# Docker Compose

Docker Compose is a tool that allows you to define and manage multi-container Docker applications using a simple configuration file (docker-compose.yml).

- Easy Networking
- Multi-Container Orchestration
- Declarative Configuration


<!-- -------------------------------------------------------------------------------- -->



---
transition: fade-out
---

# Docker Swarm

Docker Swarm is a robust, production-ready orchestration tool for multi-host deployments.

- Provides clustering and orchestration of containers across multiple hosts
- Creates an overlay network for communication across hosts. 
- Supports multi-host clusters with node roles (manager, worker).
- High fault tolerance with automatic container recovery and redistribution.


<!-- -------------------------------------------------------------------------------- -->



---
transition: fade-out
---

# kubernetes

Kubernetes (K8s) is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications.

- Simplifies deploying containers across multiple nodes.
- Dynamically scales applications based on demand (horizontal scaling).
- default container runtime is **Containerd**
- Docker images are still supported, as long as they are **OCI-compliant**.





<!-- -------------------------------------------------------------------------------- -->
---
layout: center
class: text-center
---

# Thank You

Questions ?

