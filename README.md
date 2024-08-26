# AppCat Cross Repo Boilerplate Code

This repo contains boilerplate code that needs to be present in every repository.

It uses Cruft and Cookiecutter to sync the files between the repositories.

## Add the update cronjob to a repository

If you have a repository that doesn't yet have the template in it:

```
# Change one level higher in the project you want to add the template
cd ..
cruft create https://github.com/vshn/appcat-cookiecutter -f
# be sure to match the folder name for the `app_name`
```
