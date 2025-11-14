# Лабораторная работа №6. Система контроля версий

_**Цель лабораторной работы**: изучение базовых возможностей системы
управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием._

## Ход работы

1. Так как аккаунт на GitHub уже был создан, то первым шагом необходимо сделать форк репозитория и клонировать его на компьютер.

![screen_1](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_1.png)

2. Далее была выполнена настройка клиента git, а также создан текстовый файл с помощью команды _touch_. После этого создается коммит и выгружается в локальный репозиторий.

![screen_2](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_2.png)
![screen_3](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_3.png)

3. Следующим шагом необходимо было получить историю операций для каждой из веток. Деляется это с помощью команды _git show *хэш коммита*_.

![screen_4](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_4.png)
![screen_5](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_5.png)
![screen_6](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_6.png)

4. Затем создается новая ветка и просматриваются измененения в ней с помощью команды _git log_. Затем происходит слияние с веткой master с помощью команды _merge_.с разрешением конфликтов Слияние произошло без конфликтов. 

![screen_7](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_7.png)
![screen_8](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_8.png)
![screen_9](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_9.png)

5. Чтобы рассмотреть случай, когда ветки конфликтуют, слияние необходимо произвести с форкнутой веткой _branch1_. Конфликт происходит из-за того, что в обеих ветках находится файл _mergefile_, в которм находится разная информация. Чтобы разрешить конфликт, необходимо изменить информацию в файле. Удалить разделители <<, == и >>, а также следующий текст: "информацией противоречащей ветке master". Таким образом получается разрешить конфликт.

![screen_11](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_11.png)
![screen_12](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_12.png)
![screen_10](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_10.png)

6. С помощью создания пустого текстового файла фиксируется слияние веток. Также удаляются побочные ветки и ещё одним пустым текстовым файлом фиксируются изменения. Затем эти пустые файлы удаляются с помощью команды _git rm_.

![screen_13](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_13.png)
![screen_14](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_14.png)
![screen_15](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_15.png)

7. В репозиторий были внесены изменения, а именно добавлены картинки северного сияния и заката разными коммитами. Коммит с фотографией заката был отменен с помощью команды _git revert master_.

![screen_16](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_16.png)
![screen_17](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_17.png)
![screen_18](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_18.png)

8. Вносятся изменения в текстовые файлы, деляется коммит и подгружается в репозиторий. 

![screen_19](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_19.png)

9. Cледующим шагом создается ветка для отчета _report_. Переходим в нее и начинаем оформлять отчет. Создается папка со скриншотами выполненной работы и тоже подгружается в репозиторий.

![screen_20](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_20.png)
![screen_21](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_21.png)

10. Последним шагом в лабороторной необходимо получить историю операций в форматированном виде. Сделать это можно с помощью команды _git log --pretty=format:"%h -- %cd, %an : %s"_, где: 
- %h — это сокращённый хеш коммита.
- %an — имя автора коммита.
- %ar — время, прошедшее с момента коммита.
- %s — сообщение коммита.

![screen_22](https://github.com/ElenaBeluaeva/LR6/blob/report/screens/screen_22.png)

## Лог команд

- git clone
- git config user.name
- git config user.email
- git add
- git commit -m
- git push
- git show *хэш коммита*
- git branch
- git checkout
- git log
- git merge
- git branch -d
- git rm
- git revert master
- git push --set-upstream origin 
- git log --pretty=format:"%h - %an, %ar : %s"

## Вывод

В ходе выполнения лабораторной работы были изучены базовых возможности системы управления версиями. Также был получен опыт работы с Git API и опыт работы с локальным и удалённым репозиторием. Помимо этого был поучен опыт работы с markdown синтаксисом.