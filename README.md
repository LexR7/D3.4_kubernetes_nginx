Практическое задание D3.4
1. htpasswd -c .htpasswd user1
2. Вставить содержимое файла .htpasswd в secret.yml, либо выполнить вместо применения манифеста secret.yml команду
    kubectl create secret generic auth-basic --from-file=.htpasswd
3. kubectl apply -f secret.yml -f nginx-config.yml -f nginx-deployment.yml
4. Для проверки из пода (например, kubectl exec -ti nginx-sf-deploy-998c5df8c-hb85t -- sh) выполнить
    curl sf-webserver -u user1
