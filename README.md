# cloudrun-example-api
 
This is a repository that contains an example of a Dockerized Flask API, used in the blog post [Deploying a Flask API to Google Cloud Run using Terraform]().

## Running the Docker container

Fisr, build the container with

```
docker build . -t api_test
```

Then, run the container with

```
docker run -d --env PORT=8080 -p 8080:8080 api_test
```

or run it interactively with

```
docker run --rm -it --env PORT=8080 --entrypoint bash api_test
```