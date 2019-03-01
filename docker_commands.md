## remove kubernetes containers
    docker rm $(docker ps -aq --filter name=k8s)

docker images --filter "dangling=true" -q --no-trunc

docker build -t orion/base -f base/Dockerfile .


## For Go Apps
 docker build -t orion/delegation-service --build-arg APP_NAME=delegation-service -f src/gitlab.com/orion/delegation-service/Dockerfile .