# Deploy Node.js Application on Google App Engine

This repository contains a Node.js application that is deployed on Google App Engine (GAE). Google App Engine is a fully managed serverless platform for building and deploying applications, and with this guide, you can deploy your Node.js application to GAE with ease.

Video Tutorial :   [![YouTube](https://img.shields.io/badge/YouTube-Video-green)](https://youtu.be/m7gsIPi5jBk)


## Prerequisites

Before you begin, make sure you have the following:

- **Google Cloud Account**: Sign up for a Google Cloud account if you don’t already have one.
- **Google Cloud SDK**: Install the [Google Cloud SDK](https://cloud.google.com/sdk) on your local machine.
- **Node.js & npm**: Ensure you have [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed.
- **MongoDB Setup**: Ensure that you have active MongoDB Setup.
- **App Engine Setup**: Ensure that Google App Engine is enabled for your project.

## Getting Started

1. Clone the Repository
Clone this repository to your local machine:

  ```bash
  git clone https://github.com/vishal-bulbule/Node.js-App-on-Appengine.git
cd Node.js-App-on-Appengine
```

2. Install Dependencies
Install the required dependencies for the Node.js app:

  ```bash
npm install
```

3. Update an App Engine Configuration File
Update named app.yaml at the root with your valid MongoDB URL:

```yaml
runtime: nodejs20
service: blog-app

# Optional environment variables
env_variables:
  MONGODB_URI: "mongodb+srv://techtrapture:<YOUR_DB_PASSWORD>@techtrapture.wlsbucd.mongodb.net/nodeapp" ## Add your database password

```

This configuration file tells Google App Engine to use Node.js, specifies the instance class (F2 is for a balanced compute performance), and defines the routing for static assets and dynamic URLs.

4. Deploy to Google App Engine
Authenticate your Google Cloud account and set the project you want to deploy to:

```bash
gcloud auth login
gcloud config set project [YOUR_PROJECT_ID]
```

Deploy your app to Google App Engine using the following command:

```bash
gcloud app deploy
```
This will upload your application to Google App Engine, and the deployment process will take a few minutes.

