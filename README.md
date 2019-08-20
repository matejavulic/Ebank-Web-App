# Disclaimer
***This project and its source code should be used for educational purposes only.***

# Ebank-Web-App
This is a web application for online banking with all essential features. It allows registered users to manage their bank accounts, transfer funds, get a list of all past transactions, as well as to pay their utility bills.  

# Details about the project
From a logical point of view, the system has a 3-tiered REST application architecture. It is a modular client-server architecture that consists of a presentation tier, an application tier and a data tier.

![REST](https://raw.githubusercontent.com/matejavulic/Ebank-Web-App/master/pictures/threetierrest2.png)

- **Presentation tier**  
Tier comunicates with other two tiers and holds GUI. It is built with Angular, HTML, CSS, and a TypeScript as a forntend logic. It  communicates with the other tiers through API calls.

- **Application tier**  
Handles application logic. It consists of two separate servers, Node.js server (written in JavaScript) and a Django server (written in Python). Their primary purpose is to support the application’s core functions and fetch/post user data from databases throughtout database server calls. 

- **Data tier**  
Stores user related information. The data tier consists of a two database servers:
    - MongoDB server and its database, as far as Robo 3T DBMS
    - MySQL server and corresponding database, as far as MySQL DBMS  

   MongoDB databse is, due to its non relational nature, used for storing user access credentials, refference to a user bank account number and other user-centered information.
   
   MySQL database is used to store users bank account details and all related transaction details. 



# Build
Run `ng build` to build the project. The build artifacts will be stored in the `dist/`directory. Use the `--prod` flag for a production build. 

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

# Servers
## Frontend Development Server
Run `ng serve` to start a development server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
## Backend Servers Setup
### Node Server
Run `npm run start:server` to start a Node.js server.
### MongoDB Server
Download and install:  
- MongoDB Community Server 4.2.0 from its [official website](https://www.mongodb.com/download-center/community)
- Robo 3T DBMS software from its [official website](https://robomongo.org/)  

Run `mongod` to start a MongoDB database server. Make sure you have added **mongod** daemon to the `$PATH` variable.  
If everything goes well you should see following message in CLI:  
`I NETWORK  [initandlisten] waiting for connections on port 27017`

### MySQL Server
Download MySQL Installer from its [official website](https://dev.mysql.com/downloads/installer/) and install:
- MySQL Community Server 8.0.17
- MySQL Workbench 8.0.17.  
If everything goes without errors, MySQL server daemon should be automaticly started.

### Django Server
Download and install:  
- Python 3.7.4 from its [official website](https://www.python.org/downloads/)
- Django framework with `pip install Django==2.2.4`
- Install virtual enviroment with `pip install virtualenv`
  - Launch virtualenv env in cmd
  - Start new enviroment `cd your_project virtualenv env`
  - Activate virtualenv (on Windows) `cd \env\Scripts\activate.bat`
  - Now install following Python libraries:  
    `pip install numpy pandas request`  
    
In order to run a Django server, do the following:
- Change working directory to `cd \server-python\env\pythonserver`
- Start a server with `python manage.py runserver 3002`
- To check if server works, head to http://127.0.0.1:3002/randomUserData/.

