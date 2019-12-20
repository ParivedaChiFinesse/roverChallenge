# Rover Challenge

#### Running coach using a docker image

Run `docker-compose build` while in the `docker` folder, followed by `docker-compose run coach`. The `home/coach/experiments` folder will be mounted into the `experiments` folder in this repo, so if you want to persist any experiments results, make sure they are saved to that path.