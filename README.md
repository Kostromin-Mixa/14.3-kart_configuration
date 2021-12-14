# 14.3 Карты конфигураций    
- Создал карту конфигураций    
kubectl create configmap nginx-config --from-file=nginx.conf    
kubectl create configmap domain --from-literal=name=netology.ru   

![1](https://user-images.githubusercontent.com/78191008/145956018-f7e08ac0-b58c-434a-8d7a-7f4a92f545ba.png)

- Пверка карты конфигурации    

![2](https://user-images.githubusercontent.com/78191008/145956204-2d768753-9155-4510-9af7-c6ac0cb61c18.png)   

![3](https://user-images.githubusercontent.com/78191008/145956219-d265c19a-4096-4604-8bc3-4bd0a6e30edf.png)   

Как получить информацию в формате YAML и/или JSON?   

kubectl get configmap nginx-config -o yaml   
kubectl get configmap domain -o json   

Как выгрузить карту конфигурации и сохранить его в файл?   

kubectl get configmaps -o json > configmaps.json   
kubectl get configmap nginx-config -o yaml > nginx-config.yml   

Как удалить карту конфигурации?   

kubectl delete configmap nginx-config   

Как загрузить карту конфигурации из файла?   

kubectl apply -f nginx-config.yml   
