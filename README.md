# Node Hello World

Simple node.js app that servers "hello world"

Great for testing simple deployments to the cloud

## How to create kubernete cluster and deploy
1. Create a Docker File(see Dockerfile above)
2. run command docker build -t node-hello
3. Start minikube cluster by command minikube start
4. Create pod using .yaml file (sw-deployment.yaml) then running command kubectyl apply -f sw-deployment.yaml
5. Create the image inside a kubernetes cluster by command eval $(minikube docker-env)
6. Now we need to connect these pods and easy way for it is to use services.
7. Create a service YAML file(sw-service.yaml) then running command kubectly apply -f sw-service.yaml
8. minikube service sw-service --url which will give you a url.
9. Then curl <url> Your application is now running.
