# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»  - `Макаров Денис`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

- Запустите два simple python сервера на своей виртуальной машине на разных портах
- Установите и настройте HAProxy, воспользуйтесь материалами к лекции по [ссылке](https://github.com/netology-code/sflt-homeworks/tree/main/2).
- Настройте балансировку Round-robin на 4 уровне.
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

Решение:

Результаты запуска серверов и проверки балансировки представлены на скриншотах ниже:

![Снимок54](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/82a1bb6e-ba27-4752-997d-91ad717a1d5c)

![Снимок55](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/6ef1fc55-7eb2-40aa-9496-05e42fd79462)


![Снимок50](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/2ba8f330-07a0-4604-a860-df2e123862b4)


![Снимок52](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/3ddb462b-8ed4-4f3b-928e-18f0f29cbf34)


---

### Задание 2

- Запустите три simple python сервера на своей виртуальной машине на разных портах
- Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
- HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

Решение:

Представлено на скриншотах ниже:

[Файл HAProxy](https://github.com/Makarov-Denis/Claster_and_Balance/blob/main/haproxy.conf).

![image](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/dfab28c9-183d-4c62-8b12-92a3d8ebf463)

![Снимок57](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/46a390e2-be30-465e-a340-254f895f2c4b)

![image](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/7a9f9195-121c-444d-a2dd-78ee44fae338)


![Снимок53](https://github.com/Makarov-Denis/Claster_and_Balance/assets/148921246/0ac0e663-d85b-4e2b-b231-205a9a2dec35)

---

