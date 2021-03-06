# Build it yourself
## Using Ruby/Dashing directly (while developing)
```
bundle install
dashing start
```
Visit localhost:3030 to view

## Using Dockerfile (testing before deployment)

Build the image and run it:
```
$ docker build -t dashboard .
$ docker run -t -i -d -P -p 80:80 dashboard
```
If you're running docker directly on your host linux then you should see the dashboard on localhost, if you're on windows or osx machine and running docker in a VM then the dashboard will be running on your docker-environment host's IP. You can find your docker host IP by checking docker-machine's env vars, ex. with:
```
$ echo $DOCKER_HOST
tcp://192.168.99.100:2376
```
you would point your browser to http://192.168.99.100 or similar.

# To pull and run the latest 'stable' docker image
```
$ docker run -t -i -d -P -p 80:80 mozservicesqa/dashboard
```
Visiting localhost or your docker-env IP as above. This docker image is also deployed to http://dashboard.stage.mozaws.net
