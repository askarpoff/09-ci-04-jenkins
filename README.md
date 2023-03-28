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

5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).

6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). 
По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.

7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.

8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.


