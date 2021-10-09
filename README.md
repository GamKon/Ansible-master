# Ansible-master
# Author: GamKon

Automate configuring my local VirtualBox VM servers and AWS EC2 instances with Ansible. 
Using roles, config files templates, handlers, dynamic AWS inventory, OS family detection to use appropriate commands.

Tasks:
    common:
        Changes network configuration when switching Home Wifi - Mobile hot-spot
        Checks and updates must have packages
        Mounts shared folder
    aws_cli2
        Installs AWS CLI
        Logins Dockert to ECR AWS container repository
    docker
        Installs Docker
        Adds config to allow login to Nexus repository
        Installs Portainer agent from Nexus cache repository
    java:
        Installs openjdk-11-jdk-headless depending on OS architecture
    nexus:
        Prepares server, folders structure to start Nexus docker container on a fresh system
    
vms_play.yml
    runs only common task for quick network reconfiguration
lab_play.yml
    runs all roles
