# Домашнее задание к занятию 10 «Jenkins»

## Подготовка к выполнению

1. Создать два VM: для jenkins-master и jenkins-agent.
2. Установить Jenkins при помощи playbook.
3. Запустить и проверить работоспособность.
4. Сделать первоначальную настройку.

![image](https://user-images.githubusercontent.com/108946489/227795354-fc5a0956-ff65-44ef-8d42-46eedf697816.png)


## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
![image](https://user-images.githubusercontent.com/108946489/228335858-ab004ba3-81b4-4515-abfe-1dc9e5b072f4.png)

2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
 ![image](https://user-images.githubusercontent.com/108946489/228336801-14e4a16d-5067-4dbe-afe4-004cc638f383.png)

3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.

4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.
![image](https://user-images.githubusercontent.com/108946489/228340106-71283dcc-e921-44b9-9e36-610e82fc7c17.png)

5. Создать Scripted Pipeline, наполнить его скриптом.

6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). 
По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
![image](https://user-images.githubusercontent.com/108946489/228349673-4499ca42-5b65-4783-9229-ba96a6da2271.png)

7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
![image](https://user-images.githubusercontent.com/108946489/228349502-8df1a9a7-ff87-4e7a-b03a-45769a3d106e.png)
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.

<a href='https://github.com/askarpoff/vector-role'>https://github.com/askarpoff/vector-role</a>

<a href='https://github.com/askarpoff/vector-role/blob/main/Jenkinsfile'>https://github.com/askarpoff/vector-role/blob/main/Jenkinsfile</a>

<a href='https://github.com/askarpoff/vector-role/blob/main/ScriptedJenkinsfile'>https://github.com/askarpoff/vector-role/blob/main/ScriptedJenkinsfile</a>


