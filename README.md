# k8s-nginx-php_fpm

# 使い方

## ダウンロード
```
mkdir toybox
cd toybox
git clone git@github.com:arata-honda/k8s-nginx-php_fpm.git
cd k8s-nginx-php_fpm
```

## docker image build
pwd <- toybox/k8s-nginx-php_fpm
cd docker
docker build .

## apply manifest
pwd <- toybox/k8s-nginx-php_fpm
cd k8s
kubectl apply -f php-nginx-configmap.yml

kubectl apply -f php-nginx-deployment.yml

kubectl apply -f php-nginx-service.yml

## アクセス
kubectl get service
nginxという名前でポート名が出てくるので、localhost:ポート名/test.php

で確認できます。
