# Workshop environment

This folder is a participant's own project in a hands-on workshop. The app runs on this laptop, or on Cloud Run if the participant asks for it. Use only fictional or public data.

## Google Cloud

- gcloud is already configured for this workshop: the project, the region (`europe-west4`) and the service account you act as. Read them with `gcloud config list`.
- New Cloud Run services must run as `app-runtime@<project>.iam.gserviceaccount.com` and use `--max-instances 3` or lower.
- gcloud may warn that the project lacks an `environment` tag. Ignore it: it isn't part of the workshop, and you can't change tags.

## This laptop

- Only read and change files inside this folder. Don't touch anything else on the laptop.
- Put Python environments in `.venv` in this folder. Don't install anything outside it: no `brew`, `sudo`, `npm -g` or `pip` outside `.venv`.
- Ask before deleting files.

## Boundaries

- Never run `gcloud auth ...`, `gcloud config configurations ...`, `gcloud config set` or `gcloud config unset`, and never pass `--account`, `--configuration` or `--impersonate-service-account` flags.
- Never create service account keys. If you hit a permission error, stop and report it instead of working around it.
- Ask before deleting any cloud resource.
- Ask before creating anything in Google Cloud other than a Cloud Run deploy, such as a database or a VM: it may cost money.
