# Info

Здесь будет общая инфа типа гайдов.

# Работа с Git и GitHub
## Регаемся на GitHub
Кто не зареган, заходим на https://github.com, форма регистрации справа 
(или кнопка "Sign up for GutHub" по центру, если с телефона).

## Добавление в организацию
Здесь нужно придумать, как добавлять народ. Как вариант скидывать логины в комментарии под записью в вк и потом рассылать инвайты.

## Создаем себе репозиторий
После регистрации, входа и добавления в организацию переходим по https://github.com/RTF-IVT-2018-TOAU и 
создаем себе репозиторий (место, где будут храниться ваши файлы).

Для этого:
1. Кликаем справа по кнопке New
2. В Repository name вводим свою фамилию и имя транслитом
3. В самом низу нажимаем Create repository
4. Сохраняем себе ссылку на страницу репозитория. Также его можно найти среди 
репозиториев организации по ссылке https://github.com/RTF-IVT-2018-TOAU.

## Ставим себе клиент git
### Windows
// TODO: Напиcать гайд под винду
 
### Linux
Ставим гит:
```
sudo apt install git
```
#### Для примера взят SmartGit, но можете поэксперементировать с альтернативами
```
# Ставим Java
sudo add-apt-repository ppa:webupd8team/java
sudo apt update
sudo apt install oracle-java8-installer
sudo echo 'JAVA_HOME="/usr/lib/jvm/java-8-oracle"' >> /etc/environment
source /etc/environment

# Качаем SmartGit
cd ~
wget https://www.syntevo.com/downloads/smartgit/smartgit-linux-18_1_5.tar.gz
tar -xvf smartgit-linux-18_1_5.tar.gz

# Запускаем SmartGit
smartgit/bin/smartgit.sh
```

##### В окошке смарт гита последовательно выбираем:
1. I understand and agree to all terms and conditions of the license agreement
2. Non-commercial use only (all features, but no support)
3. Next
4. Ждем несколько секунд
5. Ставим галочку снизу, нажимаем OK
6. User Name вводим логин с гитхаба, E-Mail - email, на который зарегались
7. Next и еще раз Next
8. В выподающем списке выбираем GitHub
9. Тык Generate API Token, Don't use master password, OK
10. В открывшемся браузере копируем код вида 123abcde94e7e973401d и вставляем в Code, после жмем Authenticate
11. Жмем Next, Finish

##### Теперь клонируем свой репозиторий:
1. В SmartGit одно из следующих:
  - после запуска выбираем Clone existing repository, OK
  - в главном меню Repository->Clone
  - Shift+Ctrl+O
2. Возвращаемся в браузер на страницу репозитория. Если что все репозитории можно найти здесь https://github.com/RTF-IVT-2018-TOAU.
3. Вверху, где **Quick setup — if you’ve done this kind of thing before** ищем ссылку вида:
   ```
   https://github.com/RTF-IVT-2018-TOAU/имя-репы.git
   ```
   и копируем.
4. Возвращаемся в SmartGit и вставляем в Repository URL
5. Next, Accept, Next
6. Выбираем куда сохранить
7. Finish
8. Если выскочит окошко, закройте его

Поздравляю, на этом ваша подготовка завершена! Теперь можно работать с вашим репозиторием.

## Фиксация изменений
После того как вы что либо сделали с файлами в папке своего репозитория, 
вы сможете увидеть все изменения во вкладке Files в SmartGit. Также можно увидеть детальную информацию об изменениях, 
если нажать на нужный файл.

Две самых нужных функции Git это Commit (создает точку сохранения) и Push (отправляет изменения на сервер).

Для того чтобы зафиксировать изменения (создать точку сохранения) нужно:
1. Выделить все файлы (кликнуть по любому и нажать Ctrl+A)
2. В верхнем тулбаре нажать Commit (Ctrl+K)
3. В Commit message ввести любой текст, описывающий, что вы сделали с последнего сохранения 
   (ну или просто любой набор символов, хотя бы букву q)
4. Нажать Commit (если хотите просто сохраниться) или нажать Commit&Push (если хотите сохраниться и отправить изменения на сервер)
5. Если вы не отправляли изменения на сервер, то можете для этого нажать Push на тулбаре (Ctrl+U)

Если при пуше у вас возникает ошибка 403 зайдите в главном меню Edit->Preferences (Ctrl+,), Hosting providers, 
дважды тыкните по github.com и снимите галочку с Use OAuth token...
