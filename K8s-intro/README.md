![image](https://github.com/user-attachments/assets/ad2558b9-115a-459e-a34c-e546e9ec46a0)


Kubernetes Architecture:

Kubernetes:
Kubernetes is a powerful tool for automating the deployment, scaling, and management of containerized applications. It offers features like:

TLS Secrets

RBAC (Role-Based Access Control)

Namespaces

Stateful Sets

Health Probes

Environment Secrets


Example Architecture for multiple container located in different docker hosts:

Our example setup includes three main components:

Front End

Back End

Database

![image](https://github.com/user-attachments/assets/bdb32339-358b-434f-934e-0f48a5c89cd0)

Each component runs on a Docker host with an Ubuntu operating system and uses Docker as the container engine. We demonstrate how both Kubernetes can manage these components effectively.

