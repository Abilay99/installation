# Antiplag

1. Registration - verification with mobile phone
2. Authentication&Authorization - email and password api token
3. Insert text
4. Check text
5. If user is authenticated so view list your include texts
6. If user is admin view all texts

## Backend set, installation, run, test

- Installation and settings
  - install docker, docker-compose and configure
    - installing

      ```bash
          $ sudo apt-get install build-essential
          Reading package lists... Done
          ...
          $ sudo apt-get install docker docker-compose
          Reading package lists... Done
          ...
          $ sudo addgroup docker
          $ sudo usermod -aG docker $USER
          $ newgrp docker
          $
      ```

    - after command check exists inherit user on docker group ````$ cat /ect/group | grep docker```` if exist everything is OK! else restart PC

      ```bash
          $ path_docker="$(which docker-compose)"
          $ sudo chown $USER:$USER $path_docker
          $ cd antiplag
          $ docker-compose build [Click keycup Enter]
          $ docker network create antiplag [Click keycup Enter]
          $ docker-compose up -d [Click keycup Enter]
          $ docker-compose exec web python manage.py createsuperuser [Click keycup Enter]
          Имя пользователя (leave blank to use 'root'): Admin username e.g `admin` [Click keycup Enter]
          Адрес электронной почты: Admin email e.g `admin@mail.ru` [Click keycup Enter]
          Password: Admin password e.g `admin` so at this time dont showed simbols [Click keycup Enter]
          Password (again): Re-password e.g `admin` [Click keycup Enter]
          Введённый пароль слишком похож на имя пользователя.
          Введённый пароль слишком короткий. Он должен содержать как минимум 8 символов.
          Введённый пароль слишком широко распространён.
          Bypass password validation and create user anyway? [y/N]: y [Click keycup Enter]
          Superuser created successfully.
          $
      ```

- API test
  - [Testing this.](http://127.0.0.1:8000/)
  - [Admin panel.](http://127.0.0.1:8000/admin/)
