    gcloud services enable container.googleapis.com
    gcloud container clusters create wp --num-nodes=3
    kubectl apply -f mysql-volumeclaim.yaml
    kubectl apply -f wordpress-volumeclaim.yaml
    kubectl create secret generic mysql --from-literal=password=mysql
    kubectl create -f mysql.yaml
    kubectl create -f wordpress.yaml
    kubectl create -f mysql-service.yaml
    kubectl create -f wordpress-service.yaml
