# Docker_HM3
Завдання:
Докеризувати node.js app, написавши власний Dockerfile. Запустити контейнер з обмеженнями по cpu та memory. 
Node.js app має бути доступним на 80 порті. Створити аккаунт на Docker Hub. Запушити в свій публічний репозиторій готовий image. 
Завантажити код програми та Dockerfile на Github. В README.md описати всі консольні команди

Посилання на образ: https://hub.docker.com/repository/docker/dimavolkov/app

Побудова нашого іміджу:<br>
Перейдемо до каталогу з нашим Dockerfile і виконаємо наступну команду для створення образу Docker.

![image](https://user-images.githubusercontent.com/50235747/199135268-e446e34e-96ae-4bd6-935b-61f86bd431f7.png)

![image](https://user-images.githubusercontent.com/50235747/199135332-964b4f66-d920-4d91-9574-ddf36335238f.png)

![image](https://user-images.githubusercontent.com/50235747/199135351-1210142a-9e9b-4c72-a1ab-c7385ae4133d.png)

Щоб запустити контейнер, який не з’їсть всю доступну пам’ять, можна йому обмежити ресурси(Обмежемо cpu i memory):

![image](https://user-images.githubusercontent.com/50235747/199135744-3b99a6c6-1545-424e-ba60-677e0cd73837.png)

![image](https://user-images.githubusercontent.com/50235747/199135798-c7175221-ead4-4bc1-b601-b3579994f3c5.png)

![image](https://user-images.githubusercontent.com/50235747/199135853-243b99bd-97c5-4cbc-8141-dc2086ccd95f.png)

Далі ми можемо за допомогою команди ```docker stats``` спостерігати за тим скільки ресурсів цей контейнер їсть:

![image](https://user-images.githubusercontent.com/50235747/199135940-3b42f2b5-bde8-4d70-a84a-7f17ceabc200.png)

Перевіримо логи для нашого контейнера:

![image](https://user-images.githubusercontent.com/50235747/199136007-ab988588-1ab5-4b2b-b2b8-cdcc92649710.png)

Тепер ми можемо викликати свою програму за допомогою curl:

![image](https://user-images.githubusercontent.com/50235747/199136120-942fc4cc-be58-42cc-801e-f1e424727ec5.png)

Для завантаження свого образу в створений репозиторій потрібно виконати команду ```docker login```, вказавши свій логін і пароль:

![image](https://user-images.githubusercontent.com/50235747/199136266-776afbe0-7c75-4452-9d17-dbf9fd8d27da.png)

Далі нам потрібно запушити образ у Docker Hub наступною командою:

![image](https://user-images.githubusercontent.com/50235747/199136428-f945792d-bc1d-4f62-8395-5f5608fdf997.png)

![image](https://user-images.githubusercontent.com/50235747/199136439-afc79f81-ff08-455c-93f5-83dfd919bc4b.png)

![image](https://user-images.githubusercontent.com/50235747/199136479-f8a7295a-3ce9-4db0-8f28-78e3f610d419.png)









