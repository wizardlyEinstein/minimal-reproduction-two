https://github.com/renovatebot/renovate/discussions/36098

## Current behavior

run renovate....
```
sudo docker run -it --rm --env RENOVATE_TOKEN=MY_TOKEN --env LOG_LEVEL=debug renovate/renovate:40.11.19 renovate --pr-hourly-limit 0 wizardlyEinstein/minimal-reproduction
```
get a PR with only one of the two tags updated... https://github.com/wizardlyEinstein/minimal-reproduction/pull/1 

## Expected behavior

I expected a PR with both image tags updated to v1.133.0 and have confirmed the image is available.

```
$ sudo docker image pull ghcr.io/immich-app/immich-machine-learning:v1.133.0
v1.133.0: Pulling from immich-app/immich-machine-learning
Digest: sha256:4e2f17bf9a368201e8641af1d73722cddf7a71da9afc3c14e4e9d144e3c57f67
Status: Image is up to date for ghcr.io/immich-app/immich-machine-learning:v1.133.0
ghcr.io/immich-app/immich-machine-learning:v1.133.0
```

## Link to the Renovate issue or Discussion

Put your link to the Renovate issue or Discussion here.
