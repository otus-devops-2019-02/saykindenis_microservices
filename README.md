# saykindenis_microservices
saykindenis microservices repository
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
