

# Working pypy test w/Docker

## Rando Docker Commands
- docker ps -a
- docker stop $(docker ps -a -q)
- docker rm $(docker ps -a -q)

## To Run
- sudo docker build -t compile .
- sudo docker run -p 8080:8080 -it -v /var/run/docker.sock:/var/run/docker.sock compile
Something wonky is going on with /var/run/docker.sock - It means (according to smart people) that we are polling the docker socket.
My money is on codemirror as its like a bajillion lines long. This needs ripping out of production.
