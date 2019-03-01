## list helm 
    helm --namespace test list

## delete helm release
    helm delete --purge $(helm list --namespace test | grep 'publisher' | awk '{print $1;}')

    helm delete --purge kafka-ci



## kubectl

    kubectl -n ci logs -f $(kubectl -n ci get pod | grep scoring | awk '{print $1}')
    kubectl -n ci logs -f $(kubectl -n ci get pod | grep transaction | awk '{print $1}')

## gte pods/pvc
    kubectl -n test get pods

## cleos get info
    kubectl -n test exec -it eos-event-publisher-service-0 -- cleos get info

## delete pvc 
    kubectl -n ci delete pvc datadir-kafka-ci-0 datadir-kafka-ci-1 datadir-kafka-ci

## port forward
    kubectl -n ci port-forward kafka-ci-zookeeper-0 9092:9092

    kubectl -n ci exec -it kafka-ci-0 kafka-console-consumer --bootstrap-server localhost:9092 --topic transactions

    kubectl -n ci exec kafka-ci-0 -- kafka-consumer-groups --describe --group actions-cg --bootstrap-server localhost:9092

    kubectl -n ci exec kafka-ci-0 -- kafka-console-consumer --bootstrap-server localhost:9092 --topic actions

# get configmaps
    kubectl -n ci get configmaps delegation-service-config -o yaml