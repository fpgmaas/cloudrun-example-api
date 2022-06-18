# cloudrun-example-api
 
This is a repository that contains an example of a Dockerized Flask API, used in the blog post [Deploying a Flask API to Google Cloud Run using Terraform](https://fpgmaas.com/blog/deploying-a-flask-api-to-cloudrun).

## Running the Docker container

First, build the container with

```
docker build . -t api_test
```

Then, run the container with

```
docker run -d --env PORT=8080 -p 8080:8080 api_test
```

---

[![Run on Google
Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run/?git_repo=https://github.com/fpgmaas/cloudrun-example-api.git)
