# saykindenis_microservices
saykindenis microservices repository
HW Kubernetes-2



HW Kubernetes-1

Пройдена лаба kubernetes the hard way. В процессе установлены kubectl, cfssl и cfssljson, созданы сети и правила файрволла, баллансировщик нагрущки в GCP.
Созданы манифесты для деплоя приложений и БД, проверена их запуск и работа в кластере.

HW monitoring-2
Настроен мониторинг контейнеров
Собираются и визуализируются метрики приложения и бизнес-метрики
Настроен алертинг: сообщение в канал Slack
<https://hub.docker.com/u/saykind> - ссылка на докер хаб с моими образами

HW monitoring-1
Установлен prometheus, ознакомился с базовым функционалом/
Настроен мониторинг микросервисов.
Настроен сбор метрик с помощью экспортера.
<https://hub.docker.com/u/saykind> - ссылка на докер хаб с моими образами


HW Docker-4
docker-compose изменен под кейс с множеством сетей, добавлены алиасы для корректной работы comment с DB
Создан .env-файл для параметризации переменных
Имя проекта можно задавать через project_name: name

HW Docker-3

Приложение разбито на несколько компонентов
Создан том docker для размещения на нем БД

HW Docker-2

Использован docker-machine для создания хоста в GCP
Создан образ с предоставленным приложением
Создано правило файрволла gcloud для обеспечения работы приложения
Образ загружен в docker hub
Образ запущен в локальном docker
При убийстве pid1 образ завершает работу

$ export GOOGLE_PROJECT=_ваш-проект_
$ docker-machine create --driver google \
    --google-machine-image https://www.googleapis.com/compute/v1/projects/ubuntu-os-
cloud/global/images/family/ubuntu-1604-lts \
    --google-machine-type n1-standard-1 \
    --google-open-port 5601/tcp \
    --google-open-port 9292/tcp \
    --google-open-port 9411/tcp \
logging ...
Docker is up and running!
To see how to connect your Docker Client to the Docker Engine running on this virtual machine,
run: docker-machine env logging
$ eval $(docker-machine env logging)
# узнаем IPадрес
$ docker-machine ip logging

gcloud compute firewall-rules create kibana --allow tcp:5601
