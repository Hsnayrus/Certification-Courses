<h1 style="font-size: 2.5em">Course Notes</h1>

# What is Full Stack Development?

## What is a Stack?

* They are a set of applications or technologies you use to fix a problem or create a project with a certain development focus. 
* Some Examples of stacks are:
    * __Front-End Stack__: Comprises of languages such as HTML, CSS, JavaScript. They are used together the front-end or the user interface part of a web application.
    * __Back-End Stack__: Comprises of languages such as python, frameworks such as Django and tools such as DRF.
    * __Data Stack__: A part of the back end stack, which consists of database management systems and database applications to process data.
* There are various types of stacks which comprise of different technologies/tools such as the MERN stack, LAMP stack, LEMP stack, etc.

## Back-End Stack:

* Has all the tools and technologies to create an applications core, which includes business logic, workflows and data. 
* Backend development uses languages such as Python or JavaScript, frameworks such as Django and utilities such as DRF.
* The back-end stack also builds tools, databases and caching applications.

## Front-End Stack:

* The front-End Stack has two distinct parts:
    * Web
    * Mobile
* Includes everything one would need to create a user interface of a web or mobile application that communicates with the backend. 

### Web Front-End Stack:

* To build the front end component, one should konw HTML, CSS, CSS frameworks.
* They should also figure out client side programming languages such as JavaScript, TypeScript and JS frameworks such as React.

### Mobile Front-End Stack:

* Either Android or iOS Development.

## Data Stack

* One of the most important part of any web application is the data stack or, the tools one uses to store, retrieve and process data.
* Contains SQL or NoSQL database engines, caching tools and everything required to process data. 
* MySQL, MariaDB, PostgreSQL are the most widely used database tools for the data stack. These would come under SQL database engines. 
* Some examples of NoSQL database engines are MongoDB and Firebase.
* For caching, Redis is a popular and a widely used solution.

## Full Stack

* It contains everything that allows one to:
    * Prepare the application's back-end
    * Process, retrieve and store data
    * Present that data via APIs
    * On web/mobile applications.
* A full stack developer is equally skilled in all of the different stacks. 
* Such a developer should also know some basic DevOps skills in order to deploy their web-app to Production, Staging and Development Servers.
* Should also be familiar with a version control solution, e.g. Git.

## Full Stack Developer's Responsibilities:

* A Full stack developer performs:
    * Understand the complete project and take full ownership
    * Select appropriate tools for developing the front-end back-end and database
    * Create effective user interfaces for the web or mobile environments
    * Develop APIs
    * Develop the back-end of applications
    * Store, process, retrieve data from databases
    * Create servers and manage them for development, staging and production access
    * Integrate with CI/CD workflows
    * Ensure responsiveness of applications
    * Work together with the graphics team to bring their ideas to life
    * Optimize the applications for maximum performance
    * Ensure that their application follows the best security practices
    
# N-Tier Architecture

* There is a difference between layers and tiers
* When all the different components of an application, the presentation component, the application's core component and the database component are present in different places of the an application's infrastructure, like on different servers but they still communicate to function correctly, then they are called tiers
* Layers are virtual separations of different parts of an application. 
* Tiers are also differnt parts of an application, but they are physically separated in the application infrastructure.
* In modern application development there can be any number of tiers.
* We are going to discuss:
    * 3-Tier architecture
    * 4-Tier architecture

## 3-Tier Architecture

* Is the most commonly used N-tier architecture.
* If your application's core component and data component are hosted on two different servers, then they form the two tiers out of the 3-tier architecture. 
* The third tier is the client machine(either web or mobile), where all the data is being presented.
* Together, the client machine, the application server and the database server make up a 3-tier architecture. 
* The three tiers are known as:
    * Presentation Tier
        * Also called thin clients. 
        * They don't contain business logic and only communicate with the application and present the data
    * Application Tier
        * The tier which contains the application's core or business logic is the application tier
    * Data Tier
        * The tier that deals with data is the data tier.

## 4-Tier Architecture
 
* In a web-application with a 4-tier architecture, the 4th tier is known as the delivery tier.
* This delivery tier deals with caching and delivering front-end assets to the client. E.g:
    * __Content Delivery Networks(CDN):__ They have multiple servers all across the world and help deliver a web applications HTML, CSS, JavaScript code and images to a client from the nearest physically located server.
* Since they delivery tier is physicaly separated from all the other tiers, its considered as a different tier.
* This is just an example of a  4-tier web application.
* They can be very different depending on the web applications purpose. 

## Benefits of N-tier architecture:

* Security
* Scalabiity
* Maintenance
* Improvement
* Thus application development process becomes more efficient using N-tier architecture.