# Multicontainer application
Dockerizing a React application with Node.js Postgres and NginX - dev and prod - step by step


It contains React client, Node.js backend, PostgreSQL and Nginx

You can run it in development mode: docker-compose up --build
It contains Dockerfiles for client, server which you should push to your docker hub to be able
to pull them down: docker-compose down

Here in Terraform folder I provide main.tf which create vpc, subnets, Internet gateway, NAT gateway, ec2 instance and assign nat gateway to private subnet and Internet gateway to public subnets and launch ec2 instance in public subnets.

Ansible playbook.yml is created inside Ansible folder which run inside ec2 instance and install necessary configuration such as docker, docker compose, jenkins and clone github repo and deploy the service using docker-compose up -d command.
