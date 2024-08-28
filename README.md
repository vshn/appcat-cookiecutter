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
# also, the `app_name` and folder name have to match the github project name
```

## Add the Personal Access Token to the repository

1. Login to Github with the VSHN Bot account
2. Go to Settings -> Developer Settings -> Personal Access Tokens -> Fine-grained Tokens
3. Name: AppCat + App Name
4. Expiration: 10 Years
5. Select the Component Repository and the App Repository
6. Permissions:
   Contents: read/write
   Pull requests: read/write
   Workflows: read/write
7. Add the token as `COMPONENT_ACCESS_TOKEN` to the App's repository secret
