### Building locally and pushing to dockerhub

```bash
pip install jupyter-repo2docker
docker login

GIT_PREFIX=https://github.com
GIT_USER=gregoryking
GIT_REPO=lab-template

jupyter-repo2docker \
    --no-run \
    --user-name=thedatasociety \
    --image=thedatasociety/${REPO_NAME} \
    ${GIT_PREFIX}/${GIT_USER}/${GIT_REPO}

docker push ${GIT_USER}/${GIT_REPO}

```