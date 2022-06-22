# cloudrun-example-api
 
This is a repository that contains the code used to create a Dockerized Flask API and to deploy it to Google Artifact Repository, used for [this blog post](https://fpgmaas.com/blog/deploying-a-flask-api-to-cloudrun-2). The related GitHub repository with the Flask API can be found [here](https://github.com/fpgmaas/cloudrun-example-api).

## Running the Docker container

First, build the container with

```
docker build . -t flask_api
```

Then, run the container with

```
docker run -d --env PORT=5000 -p 5000:5000 flask_api
```

## Deploying the image to Google Cloud

To deploy the Docker image to Google Cloud, simply create a new release on `main` through the GitHub UI. 
By default, the image is pushed to `europe-west4-docker.pkg.dev/my-cloudrun-api/docker-repository/my-api:<tag>`.

---

[![Run on Google
Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run/?git_repo=https://github.com/fpgmaas/cloudrun-example-api.git)
