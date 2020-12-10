## Published articles & testimonials from projects and engagements

**Invoices application**
 * ***Gold recipient of the Stevie Awards 2019 (Customer Service Success)*** - The award was accepted by one of our global stakeholders, https://www.youtube.com/watch?v=8KO-O80GbH4, who we collaborated during project development. Link to article, https://stevieawards.com/sales/ibm-customer-service-success. 
 * The ***first IBM client facing application that is only using the Cloudant database as main database*** service. We're the first team in IBM to achieve this milestone.
 
    *"... I would thank all the teams involved into this Strategic Initiative for the hard work, effort and dedication to keep the date and scope planned for this Release 1.0. This is a very big achievement and demonstration of a real cooperation between different squads that are applying Agile methodology, that is itself a success*
    
    *Allow me to **personally thank @Dela Pena, Norbert Aluba (Norbert Aluba) from Engage Support team who has worked really days and nights** during the last period to complete all the MTP activities and ... JORGE A (Jorge) who is driving us in a so complex project.”* 

    by ***Sabrina (IBM Italia - PM) May 2017***

**BCI migration** 
  * Successfully migrated the Fabric version, from v1.1 to v1.4 LTS, and IBM Blockchain Platform version, from v1.0 to v2.0. Link to the article, https://www.bci.network/post/international-business-machines-bci-in-collaboration-with-ibm-advances-blockchain-based-financial?lang=en, detailing the milestone

    *"We had a call with BCI Executives today and I’d like to personally thank you for the amazing work you did with our BCI Blockchain Network migration. I understand from the team that you have been helping 15 BCI members since end of June, with long hours of conference calls to guide our clients on the migration steps....**it’s called out as one of the best engagements we have had with them** so far. "*

    by ***Patama Chantaruck (VP For Indochina Expansion And MD Of IBM Thailand IBM) - Sep 2020***
 

## Featured projects

### 1. Budget hotel system

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

### 2. Invoices

* An internal invoicing application written in AngularJS, while the API is written in ExpressJS
* Requires internal access: https://www.ibm.com/support/customer/zz/en/invoices.html

<img width="1588" alt="invoices-01" src="https://user-images.githubusercontent.com/2144028/99945003-ce156480-2dae-11eb-8be4-d1dc591a028b.png">

### 3. Creating a new Fabric network in IBP

* This customizable script uses puppeteer to create an IBM Blockchain Platform network (IBP)
* You must create the IBP instance first then the URL and credentials will be utilized by the automated sript
* See repository: https://github.com/n0rbs/puppeteer-blockchain-platform

<img width="1638" alt="ibp-01" src="https://user-images.githubusercontent.com/2144028/99945622-e8037700-2daf-11eb-8bb7-72451c4097ec.png">

### 4. Student management API 

* Developed this RESTful API in the past few days - a total of 48hours of development
* This is an end-to-end application development, from coding to Cloud hosting deployment. 
* See repository: https://github.com/n0rbs/student-teacher-api

### 5. E-paper SPH projects

* A few publicly accessible paper which showcases the e-paper. You can view the e-paper on your mobile browser
  * The New Paper - https://epaper.tnp.sg/jr/jc.api.d.php
  * Tabla - https://www.tabla.com.sg/jr/jrpc.php

<img width="1237" alt="epaper" src="https://user-images.githubusercontent.com/2144028/101751662-7d6e6d00-3b0b-11eb-942d-fe36583269cb.png">
