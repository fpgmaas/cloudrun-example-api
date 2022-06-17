# cloudrun-example-api


## Publishing to Google Cloud Artifact Registry
 
To push a new version to registry:

First, authenticate as the service account `registry-pusher@ingka-da-fl-dev.iam.gserviceaccount.com`

Then, run:

```
docker build . -t api_test
gcloud auth configure-docker europe-west4-docker.pkg.dev 
docker tag api_test europe-west4-docker.pkg.dev/ingka-da-fl-dev/ppo-repo/api_test
docker push europe-west4-docker.pkg.dev/ingka-da-fl-dev/ppo-repo/api_test
```

## Running the Docker container

Make sure you have built the container with

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