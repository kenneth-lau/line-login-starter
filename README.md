# LINE Login Starter Application
This is a starter application to help you get started on integrating the LINE Web Login feature into your website. Web Login lets users log in to your website using their LINE account. 

## Getting started with LINE Login in Java on Heroku
Here we'll go through how you can implement Web Login on a web server using Spring Boot and Heroku.

### Requirements

 - JDK 1.8 or higher
 - Maven 3.0 or higher
 - Git
 - A free [Heroku](https://dashboard.heroku.com/) account

### Creating a Channel

To use LINE Login, you must create a Channel for your website. For information on how to create a Channel, go to the [Creating a Channel](https://developers.line.me/web-api/channel-registration) on the LINE Developers site.   

### Deploying the LINE Login starter application

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

With the "Deploy to Heroku" button, you can easily deploy the LINE Login starter application to Heroku right from your web browser by following the steps below. (For more details, see [Introducing Heroku Button](https://blog.heroku.com/archives/2014/8/7/heroku-button).)

#### Heroku configuration

1. Click the "Deploy to Heroku" button to go to the Heroku Dashboard to configure and deploy the app.
2. Enter a Heroku app name (optional).
3. Enter the following Heroku config variables.
    - **Channel ID:** Found on the "Basic information" page in the Channel Console
    - **Channel secret:** Found on the "Basic information" page in the Channel Console
    - **Callback URL:** https:// + "Heroku app name" + .herokuapp.com/auth
4. Click the "Deploy" button. Heroku then deploys this repository to a new Heroku app on your account.

#### Channel Console

- Fill in the **Callback URL** field in the "Technical configuration" page on the Channel Console. For more details, see [Technical configuration](https://developers.line.me/web-api/technical-configuration).

#### LINE Login screen

- Open the LINE Login screen (https:// + "heroku App Name" + .herokuapp.com) in your browser and log in using your LINE account.

### Viewing logs

#### Heroku CLI
- Install [Heroku CLI (Heroku Toolbelt)](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
- Log in to your Heroku account
```
$ heroku login
```

#### View logs
- Clone the source of your existing application from Heroku using Git. For more details, see [Git Cloning Existing Heroku Applications](https://devcenter.heroku.com/articles/git-clone-heroku-app).
- Use the `heroku logs` comamnd to fetch logs. For more details, see [View logs](https://devcenter.heroku.com/articles/logging#view-logs).

 ```
$ heroku git:clone -a yourapp 
$ heroku logs --tail
```
