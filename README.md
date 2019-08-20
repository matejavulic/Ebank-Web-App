# Disclaimer
***This project and its source code should be used for educational purposes only.***

# Ebank-Web-App
This is a web application for online banking with all essential features. It allows registered users to manage their bank accounts, transfer funds, get a list of all past transactions, as well as to pay their utility bills.  

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

# Details about the project

