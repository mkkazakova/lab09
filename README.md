
### Vagrant

![image](https://user-images.githubusercontent.com/125077130/236627612-72794174-e6a8-4616-9c9d-4db373341b28.png)


Скачиваем vagrant: https://developer.hashicorp.com/vagrant/downloads

Запускаем vagrant в командной строке. Проверка корректности установки:

![image](https://user-images.githubusercontent.com/125077130/236614728-ee64429b-4e53-4bf3-9bc0-4b907b4e5371.png)

### Laravel Homestead

Homestead — официальная предустановленная виртуальная машина (VirtualBox). Laravel Homestead — официальная предустановленная Vagrant-"коробка", которая предоставляет вам замечательную среду разработки без необходимости установки PHP, веб-сервера и любого другого серверного программного обеспечения на ваш компьютер.

https://github.com/laravel/homestead

Создадим папку C:\Users\<твое имя пользователя>\.homestead и перенесём файлы:
..\homestead-main\resources\Homestead.yaml
..\homestead-main\resources\after.sh 
..\homestead-main\resources\aliases
..\homestead-main\Vagrantfile
..\homestead-main\scripts/*

### PuTTY и SSH

PuTTY — это реализация SSH и Telnet для платформ Windows и Unix. PuTTY позволяет подключиться и управлять удаленным узлом (например, сервером). Для создания SSH ключей: https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

Скачиваем: putty-64bit-0.78-installer.msi

Сгенерируем с помощью PuTTY свои приватный и публичный ключи, и сохраним их в папку ~/.ssh

Приватный необходимо сохранить в двух форматах:

~/.ssh/putty_private.ppk - стандартный для PuTTY

![image](https://user-images.githubusercontent.com/125077130/236623488-341d7066-84cb-4d94-bbeb-9133b5da3998.png)

~/.ssh/id_rsa - в формате OpenSSH

<img width="236" alt="image" src="https://user-images.githubusercontent.com/125077130/236623457-e04dd681-2bed-48b9-9527-21b9b5ea0af7.png">

Публичный:

![image](https://user-images.githubusercontent.com/125077130/236623512-fadcae45-5596-4241-834f-147c4b730ca0.png)

В итоге получаем:

![image](https://user-images.githubusercontent.com/125077130/236623554-e09c9234-6f78-44e0-8c06-8709c5e9d63c.png)

### Общая папка

Создаём папку Code

![image](https://user-images.githubusercontent.com/125077130/236625600-d61acaed-51c9-498c-9e0f-9994eb4b4336.png)

Далее vagrant up в директории ~/.homestead

![image](https://user-images.githubusercontent.com/125077130/236626631-e4d87189-92a5-4905-b91f-57e75e0092dc.png)


### Подключение к серверу

В папке PuTTY запустить putty.exe

<img width="338" alt="image" src="https://user-images.githubusercontent.com/125077130/236625892-59ebf63d-3711-4590-9c9b-ba14a1771365.png">

![image](https://user-images.githubusercontent.com/125077130/236625974-52951ce4-d64e-4422-bbdb-d440f8c48837.png)

В пункте Private key file for authetication: C:\Users\<твое имя пользователя>\.ssh\putty_private.ppk Далее open

![image](https://user-images.githubusercontent.com/125077130/236626078-651859a0-e70b-494c-91d2-99de1f73bf2c.png)

В папке Code:

![image](https://user-images.githubusercontent.com/125077130/236626095-cd941ae9-6ebe-41d9-a6f5-fe6d0ca70dba.png)

![image](https://user-images.githubusercontent.com/125077130/236626106-764a8dfa-f85f-4553-861a-4704f4b1f15b.png)

### Команды с vagrant

```
# Включить машину
vagrant up           

# Выключить машину
vagrant halt   

# Выводит список всех ранее созданных ВМ
vagrant global-status

# Выводит версию vagrant
vagrant version
```

![image](https://user-images.githubusercontent.com/125077130/236626701-f644fc70-7c24-4f24-9798-63a41b0d8702.png)

![image](https://user-images.githubusercontent.com/125077130/236626752-add52a8e-de3e-43a6-bd01-8de0cf005b41.png)

![image](https://user-images.githubusercontent.com/125077130/236627157-53e7c7aa-d70a-479d-b1ed-2910b72172d6.png)
