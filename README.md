# React To-Do List

This is a simple To-Do list app done with React. All tasks are saved into browser's local storage only.

<img src="https://raw.githubusercontent.com/computationalcore/react-to-do-list/gh-pages/to-do-list.gif" alt="Todo List" style="width: 320px; height: 582px"/>


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing 
purposes. 

### Prerequisites

The project can be built with npm or yarn, so choose one of the approach bellow in case you don't 
have any installed on your system. 

* npm is distributed with Node.js which means that when you download Node.js, 
you automatically get npm installed on your computer. [Download Node.js](https://nodejs.org/en/download/)

or

* Yarn is a package manager built by Facebook Team and seems to be faster than npm in general.  [Download Yarn](https://yarnpkg.com/en/docs/install)

### Installing

To download the project follow the instructions bellow

```
git clone https://github.com/computationalcore/react-to-do-list
cd myreads
```

Install dependencies and run with:
 
npm
```
npm install
npm start
```
or

yarn
```
yarn install
yarn start
```

## Versions

v1.0 
* Default project implementation 
 
v1.1 
* Change to material UI based interface
* Task transitions animations
* Remove tasks capabilities

## **Deploying on AWS Amplify**
### **Step 1: Sign in to AWS**
- Go to [AWS Amplify Console](https://aws.amazon.com/amplify/) and sign in.

### **Step 2: Create a New App**
1. Click **“Host a Web App”**  
2. Select **GitHub**, **GitLab**, or **Bitbucket**  
3. Connect your repository  
4. Select the **branch (e.g., main/master)** for deployment  

### **Step 3: Configure Build Settings**
- AWS Amplify automatically detects React.js, but you can customize the build settings:  
```yaml
version: 1
frontend:
  phases:
    preBuild:
      commands:
        - npm install
    build:
      commands:
        - npm run build
  artifacts:
    baseDirectory: build
    files:
      - '**/*'
  cache:
    paths:
      - node_modules/**/*
```

### **Step 4: Deploy the Application**
- Click **"Save and Deploy"**  
- AWS Amplify will **build** and **host** your application  
- Once deployed, you’ll get a live URL (e.g., `https://your-app.amplifyapp.com`)