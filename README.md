Medical Navigation - Деплой

Конфигурация для развертывания на продакшен сервере.

Стек технологий:
- Фронтенд: React + Vite + Nginx
- Бэкенд: .NET 8 + PostgreSQL + RabbitMQ
- Инфраструктура: Docker + Docker Compose

Быстрый старт:
git clone https://github.com/medical-navigation/deploy.git
cd deploy
docker-compose up -d --build

Сервисы:
- Фронтенд: http://46.146.248.104:4173
- Бэкенд API: http://46.146.248.104:5000
- Swagger: http://46.146.248.104:5000/swagger
- RabbitMQ UI: http://46.146.248.104:15673

CI/CD: При пуше в main ветку автоматически деплоится на сервер.

Важные команды:
docker-compose ps - статус сервисов
docker-compose logs armnavigation - логи бэкенда
docker-compose logs frontend - логи фронтенда
docker-compose restart frontend - перезапустить фронтенд
docker-compose down && docker-compose up -d --build - полная пересборка
