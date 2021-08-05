# Lab 4.3- Documentation

# Introduction

### Links

1. **[Live Demo](https://questboardfrontend.herokuapp.com/) (Client Side: Quest Board (Admin))**
2. **[Web Documentation (Notion)](https://wngnelson.notion.site/Lab-4-3-Documentation-8957ad35470648e792ec244aacf87c66)
3. **[GIthub Repo](https://github.com/NeneWang/lab4.3) (Lab 4.3 Client Side)**
4. **[Github Repo for Lab 4.2 Server Side](https://github.com/NeneWang/lab4.2)**
5. **[Github Repo for Lab 4.3(b) Deploying automation](https://github.com/NeneWang/CISC3140-Labs/tree/main/4.3)**

The application is a quest board admin, where you can create quests, and aventurers. Log missions, delete missions, etc.

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled.png)

Screenshot from: [https://questboardfrontend.herokuapp.com/](https://questboardfrontend.herokuapp.com/)

# Automatic Deployment

To deploy the app automatically on Heroku, a makefile script is provided in the following repository:  [https://github.com/NeneWang/CISC3140-Labs/tree/main/4.3](https://github.com/NeneWang/CISC3140-Labs/tree/main/4.3)

Please follow the instructions on the Readme file.

# Data Flow

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%201.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%201.png)

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%202.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%202.png)

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%203.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%203.png)

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%204.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%204.png)

![Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%205.png](Lab%204%203-%20Documentation%208664d221e4a24ef38b502e8329b10acd/Untitled%205.png)

### Steps I took to design the layout

1. I got inspired by looking at rpg's quest boards.
2. Separated into checklist the different "features" that a guild clerk would need to have access to.
3. Drawed on paper basic sketch of the layout
4. Created layout with dummy data and no API logic
5. Added API Logic


# API

For more information about the API used, you can refer to the readme on the [repository](https://github.com/NeneWang/lab4.2) or this [notion documentation](https://www.notion.so/Lab-4-2-API-bc4c1d0b25c84a24aefecae8636e30eb)

## URL Routes Accesed

```json
https://simplenodeserver2.herokuapp.com/quests
```

For creating and fetching quests

```json
https://simplenodeserver2.herokuapp.com/users
```

For creating and fetching aventurers (users)

```html
https://simplenodeserver2.herokuapp.com/quests/:questId
```

For DELETING quests

```json
https://simplenodeserver2.herokuapp.com/complete-quest
```

For completing quests

# Setup Environments

## Setup Local Environment

**Requirements**

1. [Git](https://git-scm.com/downloads) (To clone)
2. [Node](https://nodejs.org/en/download/)

**Steps client side.**

1. Clone the repository

    ```bash
    git clone https://github.com/NeneWang/lab4.3.git
    ```

2. Open lab4.3 folder
3. Open index.html in your browser 

**Steps server side.**

1. Clone the repository

    ```bash
    git clone https://github.com/NeneWang/lab4.2.git
    ```

2. Open your terminal into the folder location
3. npm install the dependencies

    ```bash
    npm install
    ```

4. Run the server in node

    ```bash
    node index.js
    ```

## Deploy Production Ready Code

**Requirements**

1. All requirements from Setup Local Environment
2. [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

**Running a script**

Follow the instructions in: [Lab 4.3(b)](https://github.com/NeneWang/CISC3140-Labs/tree/main/4.3)

**Steps for deploying client side (Lab 4.2)**

1. Open your terminal 
2. Login into your Heroku Account

    ```bash
    heroku login
    ```

3. Enter to your server side code folder (lab4.2)

    ```bash
    cd lab4.2
    ```

4. Commit changes into a repository if you haven't yet:
    1. git init
    2. git add.
    3. git commit -m "Ready for Production"
5. Create Heroku Project

    ```bash
    heroku create questboardbackend2
    ```

6. add your remote repo to heroku
7. push remote to Heroku

    ```bash
    heroku git:remote -a questboardbackend2
    ```

8. Push to Heroku

    ```bash
    git push heroku HEAD:master
    ```

9. You can open your web application using heroku open

    ```bash
    heroku open
    ```

**Steps for deploying client side (Lab 4.3)**

1. Open your terminal 
2. Login into your Heroku Account

    ```bash
    heroku login
    ```

3. Enter to your server side code folder (lab4.2)

    ```bash
    cd lab4.3
    ```

4. Commit changes into a repository if you haven't yet:
    1. git init
    2. git add.
    3. git commit -m "Ready for Production"
5. Create Heroku Project

    ```bash
    heroku create questboardfrontend2
    ```

6. add your remote repo to heroku
7. push remote to Heroku

    ```bash
    heroku git:remote -a questboardfrontend2
    ```

8. Push to Heroku

    ```bash
    git push heroku HEAD:master
    ```

9. You can open your web application using heroku open

    ```bash
    heroku open
    ```

# Credits for Libraries and Frameworks Used:

### Client Side

- Bootstrap 4.3 [https://getbootstrap.com](https://getbootstrap.com/)
- Jquery: https://api.jquery.com/
