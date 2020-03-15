This is a template to adapt a Firebase project to Google Cloud Build.

# Prerequisites
- `gcloud` command line tool. It can be installed following the url below.

https://cloud.google.com/sdk/install

- Setting up gcloud tool with `gcloud init` linking the project connected with your Firebase project.

# How to use
1. Replace `[YOUR PROJECT ID]` strings all to your Google Cloud project id.
1. Copy `Dockerfile.template` to `Dockerfile`.
1. Get your firebase token with `firebase login:ci` command.
1. Replace `[YOUR FIREBASE TOKEN]` string in `Dockerfile` to the token fetched above.
1. Build a container for Cloud Build with `gcloud builds submit --config=image.yaml .` command.
1. Execute Cloud Build with `gcloud builds submit --config=cloudbuild.yaml .`.
1. If successful with the process above, commit this repository and push it.
