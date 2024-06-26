---
title: 'Deploy to Render.com'
description: 'Publish your website to Render.com for free'
technologies: ['postgres', 'databases','flask','node','express','react']
---

Deploying to Render.com (takes 7 minutes).

> Important: You cannot deploy this project without creating the migrations first, please run the project in your coding editor and make sure the `src/migrations` folder exists. If it does not exist, you can run `pipenv run init` or `flask db init` inside the environment. Also, make sure you have all your needed migrations by running `pipenv run migrate` or `flask db migrate` inside the environment.

## 1) Create account

[Create an account on Render.com using Github connect](https://dashboard.render.com/register?next=/). Please don't do anything else.

## 2) Create blueprint

Create a blueprint from your Github connection. [Click here](https://dashboard.render.com/select-repo?type=blueprint) and look for your project repository.

> Important: Please make sure your project contains a `render.yml` file on the root. The [4Geeks Flask + React boilerplate](https://github.com/4GeeksAcademy/react-flask-hello) comes with it.

After choosing your repository you should see a screen similar to this:

![new blueprint](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/static/img/new-blueprint.png)

## 3) Fill the form for the blueprint

Now you should see a small form with 3 questions:

- 3.1. Choose a `Service Group Name`, for example: `My First Project`. 
- 3.2. Select a `branch`, usually the `main` branch should suffice.
- 3.3. Click the `apply` blue button.

You will see a loading animation with the status of the Postgres database and the web service being built.

![loading blueprint](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/static/img/loading-blueprint.gif)

It takes several minutes to load both services, please be patient and wait until both checkmarks show up.


## 4) Set the environment variables

As you did in your local project, you will have to set the extra env vars you have added in your project in the Render settings.

Go to the Environment section in your Render's server panel and include the additional Environment Variables you need.

> 🔥 IMPORTANT: Every time you change the ENV VARs you will need to redeploy your project. ENV VARs only have an effect when the project is built again.**

## Your website is ready!

Once the deploy is finished you can go ahead and open your website:

![open your website](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/static/img/open-website.png)

## Errors? How to Troubleshoot

If you encountered an error while deploying the web service, [you can check the server logs here](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/site/static/img/blueprint-error.gif). 

Some times the deploy service has errors for no particular reason, if you believe that is your case, try [re-deploying again using a manual deploy](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/site/static/img/manual-deploy.gif). 

## Check your deploy logs

It is always recommended to check your deploy logs for errors or any other important messages, this is how a successful deploy should look like.

![success log](https://raw.githubusercontent.com/4GeeksAcademy/Templates-Boilerplates/master/static/img/success-log.png)

