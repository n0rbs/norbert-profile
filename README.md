## Featured projects

### Budget hotel dashboard

* A fully deployed and utilized hotel management system for a small apartment
* This system is composed of a single page app, written in React, and multiple micro services running on a Kubernetes cluster
* The front end is a responsive application using react-bootstrap. The app is intended to be used in a tablet device but can also be viewed in the browser
* ExpressJS was the choice for writting the API with swagger routes express as the main Swagger API middleware
* The micro services were containerized, deployed in K8s and some of them are communicating directly with each other
* The frontend (UI) and backend (APIs, ETL, Cloudant) are currently deployed in DigitalOcean's Kubernetes droplet
* The Cloudant database is also running in the k8s cluster
* An ETL processes data from a 3rd party source, dumped to a Cloudant database and then utilized by the application
* I'm using GitHub's CI/CD service, GitHub Actions, to package the apps into docker images and deploy them into the K8s cluster
* An Nginx ingress has been configured to accept http/https traffic directed to the UI (frontend) or APIs (backend)
* I'm using Let's Encrypt for my security certificates, which I use in my frontend and backend services

<img width="982" alt="cdp-01" src="https://user-images.githubusercontent.com/2144028/99944712-53e4e000-2dae-11eb-97e9-1d579d985dfd.png">
<img width="988" alt="cdp-02" src="https://user-images.githubusercontent.com/2144028/99944750-6101cf00-2dae-11eb-9e4c-b27fdb9689de.png">



**Important Note**: This is personal project that I made, on my spare time, so that I can continue to code, try new capabilities with K8s and create an application with a microservices design pattern philosphy.

### Creating a new Fabric network in IBP

* This customizable script uses puppeteer to create an IBM Blockchain Platform network (IBP)
* You must create the IBP instance first then the URL and credentials will be utilized by the automated sript
* See repository: https://github.com/n0rbs/puppeteer-blockchain-platform

### Invoices

* An internal invoicing application written in AngularJS, while the API is written in ExpressJS
* Requires internal access: https://www.ibm.com/support/customer/zz/en/invoices.html

<img width="1588" alt="invoices-01" src="https://user-images.githubusercontent.com/2144028/99945003-ce156480-2dae-11eb-8be4-d1dc591a028b.png">

