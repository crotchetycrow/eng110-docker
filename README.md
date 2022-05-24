# Docker

## What is Docker?

- Containerisation platform
- Combines source code with OS libraries and dependencies
- Simplify delivery

## What is the container lifecycle?

- 5 phases

## How does docker work?

- Packages, provisions and runs containers
- Docker images contain all dependencies
- Docker REST API
- Docker Daemon - persistent background process
- Docker client - issue build, run and stop commands
- Docker Host - responsible for running one or more containers
- Docker Engine - create and run containers

## Why adopt containerisation with docker?

- Portability - deploy to any other system
- Performance - smaller footprints and quicker to start
- Isolation - independent of one another

## What is containerisation?

- Lightweight alternative to virtualisation
- Encapsulates in a container with own operating environment
- Uses host's OS

### Benefits?

- Agility - created rapidly, deployed to any environment
- Faster delivery - big projects take less time because of compartmentalisation
- Lightweight - less resources

## What is virtualisation?

- Virtual versions of physical computing resources
- Run different OS on same hardware
- VM set up OS - no start up activities

### Benefits?

- Reduced CapEx
- Mimised downtime
- Greater disaster recovery response
- Faster provisioning of applications and resources

## Virtualisation vs Containerisation

| Virtualisation                                        | Containerisation                                      |
| ----------------------------------------------------- | ----------------------------------------------------- |
| More secure and fully isolated                        | Less secure and isolated at the process level         |
| Heavyweight, high resource usage                      | Lightweight, less resource usage.                     |
| Hardware-level virtualization                         | Operating system virtualization                       |
| Each virtual machine runs in its own operating system | All containers share the host operating system        |
| Startup time in minutes and slow provisioning         | Startup time in milliseconds and quicker provisioning |

## What is microservice architecture?

- Large application divided into separate parts
- SRP

### Benefits?

- Relatively small scale
- Independently managed
- Self-contained and independently deployed
- Supports horizontal scaling
- Can use different technology

### Disadvantages?

- Less secure
- Debugging is difficult (control flow)
- More complex than monolithic applications
- High network usage cost

## What is monolithic architecture?

- Application built in one unified model

### Benefits?

- Simple to develop relative to microservice
- Easier to deploy (single)
- Relatively easier and simpler to develop
- Less network and latency problems

### Disadvantages?

- Too large
- Redeploy whole
- The bigger it is, slower it is
- Difficult to understand for new joiners
