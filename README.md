# DataCenterProgramming
### 데이터센터프로그래밍 과제3  

Mongo DB, Mongo Express를 사용하여 pods 간의 통신을 보여주려 함.
- Web application과 DB의 communication을 잘 보여줄 수 있는 간단한 예시.  

![진행 과정](https://user-images.githubusercontent.com/73309550/101239352-49213800-372a-11eb-8ab1-41796813504d.PNG)  


### kubectl apply commands in order
    
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f mongo-configmap.yaml 
    kubectl apply -f mongo-express.yaml

### kubectl get commands

    kubectl get pod
    kubectl get pod --watch
    kubectl get pod -o wide
    kubectl get service
    kubectl get secret
    kubectl get all | grep mongodb

### kubectl debugging commands

    kubectl describe pod mongodb-deployment-xxxxxx
    kubectl describe service mongodb-service
    kubectl logs mongo-express-xxxxxx

### give a URL to external service in minikube

    minikube service mongo-express-service
