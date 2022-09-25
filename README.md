# Публикация приложения в [NashStore](https://store.nashstore.ru/)
## Введение
Система Android позволяет устанавливать приложения при помощи других приложений (магазинов или сторов). В таком случае разработчик может распространять, обновлять и рекламировать своё приложение, используя возможности стора.

Для примера рассмотрим магазин приложений [NashStore](https://store.nashstore.ru/). Он отлично подойдёт для начинающих, потому что для регистрации не требуется оплачивать регистрационный сбор в отличии от [Google Play](https://play.google.com/) и не нужно иметь предприятие как в [RuStore](https://rustore.ru/)

## Регистрация
Для использования NashStore нужно пройти регистрацию для доступа к магазину и отдельно регистрацию аккаунта разработчика
Переходим на страницу регистрации https://store.nashstore.ru/profile/sign_up
Вводим свои данные
<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192158188-07c12195-03aa-4704-b2fc-f772f5a59288.png">

После успешной регистрации нужно подтвердить email

Далее регистрируем аккаунт разработчика

<img width="223" alt="image" src="https://user-images.githubusercontent.com/13727567/192158442-34572bb4-875d-461a-8603-6338cb3b70ba.png">
Заполняем анкету

![image](https://user-images.githubusercontent.com/13727567/192158539-784294ab-f29c-4f56-a744-467a02532d69.png)

И нажимаем "Создать аккаунт"

![image](https://user-images.githubusercontent.com/13727567/192158645-dcb42a3e-5603-42a7-b37f-5d7646b047c5.png)

Аккаунт зарегистрирован, но потребуется некоторое время для проверки

![image](https://user-images.githubusercontent.com/13727567/192158725-b4d8d65a-07d3-4599-bd55-c8ce8396d7fe.png)

В это время мы можем подготовить наше приложение к публикации

## Подготовка

На данном этапе от нас потребуется:
- минимум 2 скриншота
- большая иконка приложения (создаётся при генерации иконки). [Пример](https://github.com/netology-code/andad-code/blob/master/01_di/android/app/src/main/ic_launcher-playstore.png)
- apk файл, собранный в release версии

Переходим к [консоли разработчика](https://store.nashstore.ru/console), выбираем созданный аккаунт

Нажимаем "Создать приложение"

![image](https://user-images.githubusercontent.com/13727567/192159170-6275db4c-b5a3-45f9-a8fc-daa32b0b5110.png)

![image](https://user-images.githubusercontent.com/13727567/192159245-6fbba379-8ab5-47e5-b3d2-55fd2ea6fde3.png)

Заполняем информацию, которую увидит пользователь

![image](https://user-images.githubusercontent.com/13727567/192159302-ded94be2-0360-4a08-988f-9814c897b4af.png)

![image](https://user-images.githubusercontent.com/13727567/192159363-eba261d9-0765-47cb-b0cd-959925de28e9.png)

Далее укажем информацию, которая потребуется при возникновении вопросов по приложению

![image](https://user-images.githubusercontent.com/13727567/192159488-6e45a47e-c921-45cf-821d-ab385e3586e8.png)

Потребуется иконка и скриншоты

![image](https://user-images.githubusercontent.com/13727567/192159560-8b1dc28a-8510-4f01-a524-8f1f5d685362.png)

Поскольку в приложении есть функции, доступные только после аутентификации, необходимо завести тестовый аккаунт и поделиться им. Необходимо для проверок и одобрения публикации со стороны магазина

![image](https://user-images.githubusercontent.com/13727567/192160053-bbe3fcc3-85fb-43fb-b6dd-6e10092f10ba.png)

# Публикация

Переходим к вкладке "Управление выпусками" и создаём выпуск

![image](https://user-images.githubusercontent.com/13727567/192160239-03355a31-e45a-491e-bcdf-c325f4a3d461.png)

На данном этапе нам потребуется подписанная релизная сборка. Напомню как её получить

Перед сборкой необходимо придумать уникальный applicationId. 

<img width="646" alt="image" src="https://user-images.githubusercontent.com/13727567/192161982-23135a2d-d298-4f1c-a052-fa76e1229dda.png">

Как правило applicationId представляет собой имя сайта наоборот. При этом доменное имя сайта не обязательно должно вам принадлежать. Он должен быть уникален в рамках магазина приложений

Для сборки релиза в Android Studio нужно выбрать данный пункт

<img width="317" alt="image" src="https://user-images.githubusercontent.com/13727567/192160379-7b8c45b3-134c-4f8f-91f0-7916ba7b4c17.png">

В появившемся окне выбираем Apk

<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192160418-e5fe8833-5252-470a-8b19-17e505858475.png">

Если на данном этапе есть хранилище ключей (keysore), то можно выбрать существующий. Если нет, то нужно создать (Create New)

<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192160533-d4f19cea-bb96-4bd4-b4b6-ac5c89f1128b.png">

При создании keystore указывайте свои данные, которые могут идентифицировать вас как автора. Время жизни ключа побольше (25 лет хватит)

<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192160622-c035ba7a-fdd8-49da-8470-b39c03d1f90c.png">

После создания/выбора keystore переходим далее (Next) и выбираем release

<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192160682-05a1da0c-2214-4e84-8a37-aa909e54b9b3.png">

Готовый apk должен быть здесь:

<img width="620" alt="image" src="https://user-images.githubusercontent.com/13727567/192161676-68f163c8-2082-4486-8619-5d3891fb3255.png">

В появившемся окне выбираем созданный ранее Apk

![image](https://user-images.githubusercontent.com/13727567/192160324-98d7fa76-b583-46df-9cd0-4e8b3d6bc84b.png)

Выпуск можно опубликовать

![image](https://user-images.githubusercontent.com/13727567/192162310-3d3d8d49-d10a-4c13-b92b-2636d6d77df9.png)

К каждому выпуску можно указывать краткое описание о том, что изменилось

![image](https://user-images.githubusercontent.com/13727567/192162418-73e9c388-0c92-4129-8292-14503f8684e1.png)

Заключительный этап

![image](https://user-images.githubusercontent.com/13727567/192162513-71ab43f1-7de4-4a97-9f64-b627f19120db.png)

Ждём одобрения
