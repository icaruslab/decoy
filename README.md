# Decoy

Decoy is a reverse-proxy written in python and ready to to deploy on Google App Engine platform. It can be configured to serve a specific website through App Engine.

The main advantage Decoy provides is the ability to serve the configured website through GAE platform, using a sub-domain under appspot.com domain.

**Decoy will proxy all URLs which contains the configured domain in config.py automatically, any other URL will be opened normally without proxy.**

**Usage**

1. Create an account on [Google Cloud Platform](https://cloud.google.com/)
2. After accessing [Google Cloud Console](https://console.cloud.google.com/) create a new project
3. Install [Google Cloud SDK](https://cloud.google.com/sdk/install)
4. Clone the project
5. Change the `url` variable in config.py
6. Use your terminal to go the project's directory
7. Run `gcloud init` to configure GCloud SDK and login to your account.
8. Select the project you created earlier using `gcloud config set project $project_name`
9. Run `gcloud app deploy` and follow the instructions to deploy the app
10. Finally you can confirm your mirror is running by visiting `[youprojectname].appspot.com`

**Why Google App Engine?**

The main advantage of having the mirror traffic routed through GAE, is the ability to use a sub-domain under appspot.com to access the mirror.

As the same domain is associated with many other Google cloud services it'd be difficult to block it altogether. However, it's possible to block the sub-domain without having to block the entire domain name, in which case you'll be able to get a new mirror up and running in less than two minutes by simply creating a new project with a different name and repeating steps 8:10

**Attribution**

This project was inspired and built on [mirrorrr](https://github.com/bslatkin/mirrorrr) project.

**Todo**

- [ ] Rewrite in Python3
