## Запуск контейнеров приложений

### Локальный istin.pro для разаработки
* Установить Ubuntu (У меня 16)
* sudo apt-get install git
* Зерагеаться на gitlab.com
* git config --global user.name "sklukin"
* git config --global user.email sklukin@yandex.ru
* sudo sh -c "echo '127.0.0.1 istin-dev.pro' >> /etc/hosts"
* Поставить docker. [Инструкция](https://docs.docker.com/engine/installation/linux/ubuntu/)
* Docker не для root [Инструкция](https://docs.docker.com/engine/installation/linux/linux-postinstall/)
* Проверка докера `docker run hello-world`
* Получить у sklukin доступы к репке
* mkdir some_dir
* cd some_dir
* git clone git@gitlab.com:sklukin/istin.pro.git
* git clone git@gitlab.com:sklukin/docker.git
* cd docker
* make istinpro
