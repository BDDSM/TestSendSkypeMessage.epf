# TestSendSkypeMessage.epf

Пример отправки сообщений в skype из 1С [СКАЧАТЬ](https://github.com/kuzyara/TestSendSkypeMessage.epf/releases/download/1.0/TestSendSkypeMessage.epf)

**Как получить ID и пароль бота?**
1.    Заходим на страницу https://dev.botframework.com/bots/new, предварительно залогинившись под учеткой microsoft
2.    Заполняем поля: Display name, Bot handle, Long description, включаем Enable adding to a group.
3.    Нажимаем «Create Microsoft APP ID and password» - копируем идентификатор  приложения (ID приложения). Нажимаем «Создать для приложения» - копируем отображенный пароль (токен)  – нажимаем «завершить и вернуться» - Registred
4.    Сохраняем данные в блокнотик
5.    Добавляем бота к себе в контакты, перейдя по ссылке вида https://join.skype.com/bot/cffbb6ea-1f54-4d57-9d5b-1f04cedd228a (кнопка Get bot embed codes)

**Как получить ID беседы (группы, контакта)?**
1. Идем на Webhook Tester и получаем ссылку вида 
https://webhook.site/cfd9261e-a3d8-410f-8547-da9628390339
2. Вставляем эту ссылку в Messaging endpoint на странице настроек чат-бота, сохраняем
3. Пишем в скайпе из группы (айди которой хотим получить) сообщение боту вида "@botname test", где botname - имя созданного бота
4. Получаем в вебхук-тестере пост-запрос с джисоном, нужый нам айди находится в поле conversation.id

**Как использовать?**
```
Токен = ПолучитьТокенSkype("cffbb6ea-1f54-4d57-9d5b-2f04cedd228a", "jisp8}^{tyuTHHKTJ5547"); // айди и пароль бота
IDЧата = "29:2b9b13504f134aebad59a25a7bdc1f98@thread.skype"; // айди комнаты
ТекстСообщения = "Привет, мир!";
ОтправитьСообщениеSkype(Токен, IDЧата, ТекстСообщения);
```

![2019-04-01_18-00-12](https://github.com/kuzyara/TestSendSkypeMessage.epf/blob/master/2019-04-01_18-00-12.png?raw=true)

**Видео как добавить бота в группу (youtube)**

[![Добавление бота в группу](https://img.youtube.com/vi/mT5Wd_BJJRw/0.jpg)](https://www.youtube.com/watch?v=mT5Wd_BJJRw)
