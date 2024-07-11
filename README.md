# CI/CD Trial for Docker with Python Application

This is my first successful CI/CD trial repository for **Docker**, including a Python script, a `Dockerfile` and a workflow file that has commands to push everything to my personal Docker Hub whenever any change occurs here.

After encountering several errors and fixing them, the workflow is now being executed without any issues. As a result, I'm able to see the image related to these repository in my Docker Hub!

For this to work, I've followed all the steps explained in this official Docker Guide:

Language-specific Guides > Python > Configure CI/CD

[Click here to read](https://docs.docker.com/language/python/configure-ci-cd/)

### Important

When all the steps are carried out and the workflow is executed, it may end with **failure** in GitHub Actions, because there is no `Dockerfile` found! Thus, you need to create one on your own, then commit & push to the remote repository. This is something that the official guide forgot to tell!

This is my content inside `Dockerfile`:

```
FROM python:3
WORKDIR /usr/src/app
COPY . .
CMD ["python", "./app.py"]
```