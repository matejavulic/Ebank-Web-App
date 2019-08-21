# Disclaimer
***This project and its source code should be used for educational purposes only.***
***A fictional names "Ebank", "E-bank", "Ebanka", "E-banka" as far as fictional bank logos have been used only for representative purposes.***

# Ebank-Web-App
This is a web application for online banking with all essential features. It allows registered users to manage their bank accounts, transfer funds, get a list of all past transactions, as well as to pay their utility bills.  

# Project Details
## Logical Structure
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

   MongoDB databse is, due to its non relational nature, used for storing user access credentials, reference to a user bank account number and other user-centered information.
   
   MySQL database is used to store users bank account details and all related transaction details. 

## Presentation tier
### Frontend
- Frontend design principles  
  User interface design was conducted according to the usability guidlines given in [10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/) by Jacob Nielsen. It recommends following heuristcis for UI design:
  - 1: Visibility of system status  
    *The system should always keep users informed about what is going on, through appropriate feedback within reasonable time.*  
    
    Examples (left picture - Sign In visibility status, right picture - Recent Transactions visibility status):   
    ![REST](https://raw.githubusercontent.com/matejavulic/Ebank-Web-App/master/pictures/fetch.PNG)
    ![REST](https://github.com/matejavulic/Ebank-Web-App/blob/master/pictures/fetching%202.PNG)

  - 2: Match between system and the real world  
     *The system should speak the users' language, with words, phrases and concepts familiar to the user.*  
     
     One way to accomplish this requirement is to use methapore to symbolicly represent apstarct idea of real world expirience. For example, opposite arrows icon can be a good real life metaphore for banking transactions:
     ![REST](https://raw.githubusercontent.com/matejavulic/Ebank-Web-App/master/pictures/methaphore.PNG)
     
  - 3: User control and freedom  

  - 4: Consistency and standards  
  *Users should not have to wonder whether different words, situations, or actions mean the same thing.*  

    During frontend develpoment, [Google Material Design](https://material.io/design/introduction/#principles) principles were followed.

  - 5: Error prevention  
  
  - 6: Recognition rather than recall  
  *Minimize the user's memory load by making objects, actions, and options visible.*  

    Stylized door icon can be a good replacement for Sing Out label:  
  ![REST](https://raw.githubusercontent.com/matejavulic/Ebank-Web-App/master/pictures/recognize.PNG) 
   
  - 7: Flexibility and efficiency of use  
  *Accelerators — unseen by the novice user — may often speed up the interaction for the expert user. Allow users to tailor frequent  actions.*

  - 8: Aesthetic and minimalist design  
  *Dialogues should not contain information which is irrelevant or rarely needed. Every extra unit of information in a dialogue competes with the relevant units of information and diminishes their relative visibility*.

  - 9: Help users recognize, diagnose, and recover from errors  
  *Error messages should be expressed in plain language (no codes), precisely indicate the problem, and constructively suggest a solution.*

 - 10: Help and documentation  
 *Even though it is better if the system can be used without documentation, it may be necessary to provide help and documentation. Any such information should be easy to search, focused on the user's task, list concrete steps to be carried out, and not be too large.*

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

