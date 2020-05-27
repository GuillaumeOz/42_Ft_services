# 42_Ft_services

`ft_services` is an individual school project at [42 Paris](https://www.42.fr) campus.
The purpose of this project is to use Kubernetes to virtualize a network and set a production environment.

## Introduction

<p align="center">
  <img src="assets/Work in progress.gif" alt="demo gif" width="800" />
</p>

For learning purposes only, **not intended for production**.

## Components

* Alpine Linux
* Kubernetes
* Docker
* Ingress Controller
* Nginx
* FTPS
* WordPress
* phpMyAdmin
* MariaDB (MySQL)
* Grafana
* InfluxDB

### Linux Alpine

We run our project on **Linux Alpine** which uses the Linux kernel.  
Alpine Linux is a security-oriented, lightweight Linux distribution based on musl libc and busybox.  
This distribution is particularly suitable, due to its lightness, for the creation of Docker container images.  
[More details here](https://wiki.alpinelinux.org/wiki/Alpine_Linux:FAQ).

### Kubernetes and Minikube

**Kubernetes** is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.  
[More details here](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)  Or [Here](https://medium.com/@tsuyoshiushio/kubernetes-in-three-diagrams-6aba8432541c).  
  
**Minikube** is a tool to facilitate the local execution of Kubernetes. Minikube runs a single-node Kubernetes cluster in a virtual machine (VM) on your laptop.  
[More details here](https://kubernetes.io/docs/tutorials/hello-minikube/).

### Nginx

**Nginx** is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers.

### Kubernetes Ingress

In Kubernetes, an **Ingress** is an object that allows access to your Kubernetes services from outside the Kubernetes cluster. You configure access by creating a collection of rules that define which inbound connections reach which services.

if you have difficulty to understand the **interaction between Kubernetes Ingress and NGINX**, please look at this [link](https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-ingress-guide-nginx-example.html).

### Docker

**Docker** is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package.
[More details here](https://blog.usejournal.com/what-is-docker-in-simple-english-a24e8136b90b).  
For more informations, you can also check my project `ft_server` about docker containers and docker files usage [Here](https://github.com/GuillaumeOz/42_Ft_server/).  

### Wordpress

**WordPress** (WordPress.org) is a content management system (CMS) based on PHP and MySQL that is usually used with the MySQL or MariaDB database.

### PHPMyAdmin

**PhpMyAdmin** is a free software tool written in PHP, intended to handle the administration of MySQL over the Web.
It will help to link our databases with the rest ouf our services.

### MySQL

**MySQL** is a freely available open source Relational Database Management System(RDBMS) that uses Structured Query Language (SQL).
WordPress requires MySQL to store and retrieve all of its data including post content, user profiles, and custom post types.

### FTPS

**FTPS** is a name used to encompass a number of ways in which FTP software can perform secure file transfers. Each involves the use of a security layer below the standard FTP protocol to encrypt data.

### Grafana

**Grafana** is a multi-platform open source solution for running data analytics, pulling up metrics that make sense of the massive amount of data, and monitoring apps through customizable dashboards. Available since 2014, the interactive visualization software provides charts, graphs, and alerts when the service is connected to supported data sources.

### InfluxDB

**InfluxDB** is an open-source time series database(TSDB) developed by InfluxData. It is written in Go and optimized for fast, high-availability storage and retrieval of time series data in fields such as operations monitoring, application metrics, Internet of Things sensor data, and real-time analytics. It also has support for processing data from Graphite.
In our project, InfluxDB will stock the necessairy data for running Grafana application.

# REDO THIS PART WITH setup.sh
### Common tasks

* `make up` builds the image and runs it as a container
* `make clean` removes the image and the container
* `make autoindex-on` enables directory listing
* `make autoindex-off` disables directory listing

# REDO THIS PART WITH setup.sh

### Acknowledgements

School project done at [42 Paris](https://www.42.fr).

WordPress theme: [Cyanotype](https://wordpress.org/themes/cyanotype/) By Automattic.