## Purpose of this repository

This repository contains Tekton pipelines and trigger to build an example golang and python image, based off the FRSCA guidelines.

These pipelines have been tested on a single node k3s instance, and deployed using the quickstart guide at https://buildsec.github.io/frsca/docs/getting-started/introduction/

### Contents

/pipeline: contains a Tekton pipeline to build a secure Go image. The source code can be found deployed under the supplied Gitea repository under frsca/example-golang

/python_pipeline: contains a Tekton pipeline to build a secure Python image.

/pipeline/example-python-code: contains a sample Flask application, a test and a Dockerfile to build the image. Used with the python pipeline

/triggers: contains the Tekton trigger bindings, event listenere and trigger templates. The triggers will start a pipeline when a push event is detected within the git repository