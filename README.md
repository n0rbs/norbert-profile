## Featured work

### Budget hotel dashboard

* A fully deployed and utilized hotel management system for a small apartment
* This system is composed of a single page app, written in React, and multiple micro services running on a Kubernetes cluster
* The micro services were containerized, deployed in K8s and some of them are communicating directly with each other
* The UI and backend are currently deployed in DigitalOcean's Kubernetes droplet
* An ETL processes data from a 3rd party source, dumped to a Cloudant database and then utilized by the application
* I'm using GitHub's CI/CD service, GitHub Actions, to package the apps into docker images and deploy them into the K8s cluster
* An Nginx ingress has been configured to accept http/https traffic directed to the UI (frontend) or APIs (backend)
* I'm using Let's Encrypt for my security certificates, which I use in my frontend and backend services

**Important Note**: This is personal project that I made, on my spare time, so that I can continue to code, try new capabilities with K8s and create an application with a micro service philosphy.


