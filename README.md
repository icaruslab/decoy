# Decoy

Decoy is a reverse-proxy written in python and ready to to deploy on Google App Engine platform. It can be configured to serve a specific website through App Engine.

The main advantage Decoy provides is the ability to serve the configured website through GAE platform, using a sub-domain under appspot.com domain.

**Decoy will proxy all URLs which contains the configured domain in config.py automatically, any other URL will be opened normally without proxy.**

## Usage

1. Clone the project `git clone https://github.com/icaruslab/decoy.git`
2. Create an account on [Google Cloud Platform](https://cloud.google.com/)
3. After accessing [Google Cloud Console](https://console.cloud.google.com/) create a new project
4. Install [Google Cloud SDK](https://cloud.google.com/sdk/install)
5. Clone the project
6. Change the `url` variable in config.py
7. Use your terminal to go the project's directory
8. Run `gcloud init` to configure GCloud SDK and login to your account.
9. Select the project you created earlier using `gcloud config set project $project_name`
10. Run `gcloud app deploy` and follow the instructions to deploy the app
11. Finally you can confirm your mirror is running by visiting `[youprojectname].appspot.com`

## Why Google App Engine?

The main advantage of having the mirror traffic routed through GAE, is the ability to use a sub-domain under appspot.com to access the mirror.

As the same domain is associated with many other Google cloud services it'd be difficult to block it altogether. However, it's possible to block the sub-domain without having to block the entire domain name, in which case you'll be able to get a new mirror up and running in less than two minutes by simply creating a new project with a different name and repeating steps 8:10

## Attribution

This project was inspired and built on [mirrorrr](https://github.com/bslatkin/mirrorrr) project.

## Disclaimer

This project and all Icarus Project’s related products are solely focused and intended to be used as Internet censorship circumvention solutions, more specifically in human rights and independent media context.
Icarus Project is not responsible for any abuse and/or malicious use of any of its published research results.

## Todo

- [ ] Rewrite in Python3
