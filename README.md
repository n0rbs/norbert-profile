## Featured projects

### Budget hotel system

A fully deployed and utilized hotel management system for a small apartment. This system is composed of a single page app, written in React, and multiple microservices running on a Kubernetes cluster. IOT devices are also setup to automate lights based on guest schedule.

**Frontend**
* **Responsive SPA** - The frontend single page app, written in React, is a responsive application leveraging react-bootstrap. The app is intended to be used in a tablet device but can also be viewed in the browser.
* **Mobile app web view** - A simple iOS app (dev mode), which loads the web application's URL, is used by the end-user. Accessing it directly via browser, in the tablet, is also an alternative way of using it.
* **Components** - Content list, view and forms are the main building block components.

**Backend services**
* **RESTFul API** - ExpressJS was the choice for writting the API with swagger routes express as the main Swagger API middleware. Dedicated APIs were written for each apps to only cover it's business purpose or there's a separation of concerns.
* **Data service** - A Cloudant database was provisioned to hold the processed data and store inputted information from the user. A statefulset resource was defined to create the data service.
* **Service interactivity** - Some services communicate with each other to perform data processing or retrieving information
* **ETL** - Data from a 3rd party source is extracted, formatted and dumped to a Cloudant database. The processed data is consumed by the API or the other backend jobs.
* **IOT devices** - Cron jobs trigger smart lights and/or smart plugs to turn on/off based on the guest information.

**CI/CD**
* **Containerization** - I'm using GitHub Actions to build the docker images, package and deploy them to the GitHub docker respository. All UI, API and cron job services are containerized.
* **Packaging the apps** - Using GitHub's packaging service, I maintain two images, latest and second newest tag. Once a new version is released, the oldest version will be purged.

  <img width="312" alt="packages-01" src="https://user-images.githubusercontent.com/2144028/100062214-383f0f80-2e6a-11eb-83db-97e7286a25bc.png">
* **Deployment** - A custom DigitalOcean plugin is installed in the pipeline to allow GitHub actions access to the kubernetes cluster.

**Cloud infrastructure and networking**
* **Kubernetes cluster** - The UI, APIs, cron jobs, ETL, and Cloudant are currently deployed in DigitalOcean's Kubernetes droplet. Each app has it's own pod. Pods communicate via service resource or accessing the internal route.
* **Load balancer** - A load balancer was required to handle the traffic coming in. Traffic will be directed to the Nginx ingress controllers. Another 3rd party domain service hanlder manages the domain and configuration.
* **Nginx ingress** - Specific requests coming from the client app will be handled by the nginx ingress controller. A specific route will be directed to a specific API's k8s service resource. 
* **SSL** - I'm using Let's Encrypt for my security certificates, which I use in my frontend and backend services.

**Architecture**

<img width="1274" alt="architecture-01" src="https://user-images.githubusercontent.com/2144028/99978822-64fb1480-2de1-11eb-89b2-531c2dd92d54.png">

**Dashboard application**

<img width="982" alt="cdp-01" src="https://user-images.githubusercontent.com/2144028/99944712-53e4e000-2dae-11eb-97e9-1d579d985dfd.png">
<img width="988" alt="cdp-02" src="https://user-images.githubusercontent.com/2144028/99944750-6101cf00-2dae-11eb-9e4c-b27fdb9689de.png">



**Important Note**: This is personal project that I made, on my spare time, so that I can continue to code, try new capabilities with K8s and create an application with a microservices design pattern philosphy.

### Creating a new Fabric network in IBP

* This customizable script uses puppeteer to create an IBM Blockchain Platform network (IBP)
* You must create the IBP instance first then the URL and credentials will be utilized by the automated sript
* See repository: https://github.com/n0rbs/puppeteer-blockchain-platform

<img width="1638" alt="ibp-01" src="https://user-images.githubusercontent.com/2144028/99945622-e8037700-2daf-11eb-8bb7-72451c4097ec.png">

### Invoices

* An internal invoicing application written in AngularJS, while the API is written in ExpressJS
* Requires internal access: https://www.ibm.com/support/customer/zz/en/invoices.html

<img width="1588" alt="invoices-01" src="https://user-images.githubusercontent.com/2144028/99945003-ce156480-2dae-11eb-8be4-d1dc591a028b.png">

