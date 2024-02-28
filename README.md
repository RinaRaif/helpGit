# helpGit
Список базовых команд
- pwd : Показать текущую рабочую директорию (папку, из которой выполняется команда);
- ls : Отобразить файлы и папки в текущей директории;
- l -a : Отобразить файлы и папки в текущей директории, в том числе скрытые;
- cd HelpGit :  Перейти в папку;
- cd cd first-project/test : Перейти в папку test внутри папки;
- cd .. : Перейти на уровень выше (в родительскую папку);
- cd ~ : Перейти в домашнюю папку (например /users/practicum);
- mkdir second-project : Создать папку second-project
- rm hello.txt : Удалить файл hello.txt
- rmdir images : Удалить папку images
- rm -r second-project : Удалить папку и все содержиомое
- touch hello.txt : Создать файл в текущей папке
- touch hello.txt hello2.txt hello3.txt : Создать несколько файлов
- echo <текст> % Вывести текст на экран, например
- echo <текст> >> <файл>: Вывести текст в файл, например
- cat practicum.txt : Вывести содержимое файла на экран
- cp helloPracticum.txt practicum.txt : Копировать файлы и папки.
- mv <источник> <назначение> : Переместить/переименовать файлы и папки
- tail <файл> : Показать последние строки файла
- history : Показать историю введённых команд
- head <файл> : Показать первые строки файла
- man <команда> : Показать руководство по команде
- clear : Очистить экран терминала
- rm -rf ~/Library/Developer/Xcode/DerivedData : Удалить папку DerivedData. Папка DerivedData обычно содержит временные файлы, созданные Xcode в процессе сборки и запуска проектов: скомпилированные бинарные файлы, индексы для ускорения поиска и кэшированные данные. Удаление этой папки может быть полезным, чтобы освободить место на диске или решить некоторые проблем, связанные с Xcode. При следующем запуске Xcode воссоздаст необходимые файлы в этой папке.

Полезные лайфхаки Tab для автодополнения
Чтобы не вводить названия файлов и папок полностью, можно начать писать их имя и нажать клавишу Tab . Командная строка допишет путь сама, если соответствующий файл или папка есть в текущей директории.
Например, находясь в папке
dev , начните вводить cd first и нажмите Tab . Если папка first-project есть
внутри dev , то командная строка автоматически подставит её имя. Останется только нажать Enter .
История команд
Клавиша ↑ (стрелка вверх) позволяет просматривать историю ваших команд. Это удобно, когда вам нужно повторить или немного изменить предыдущую команду. Можно пользоваться стрелками ↑↓ для поиска команды, а затем ещё раз её выполнить.
Перенаправление вывода в файл
Вспомогательные команды вроде > и >> позволяют перенаправлять вывод команд в файлы. Например, ls > files.txt сохранит список файлов в файл files.txt .
Отмена текущего ввода
Cпринт 3. Командная строка 3
Если вы начали вводить команду и хотите ее отменить, нажмите Control + C . Это вернёт вас к чистому приглашению командной строки.
Повторение последней команды
Чтобы повторить последнюю введённую команду, можно ввести !! Навигация курсором
Чтобы быстро исправить введенное в начале строки, можно использовать Control + A — команда переместит курсор в начало строки. Обратная
команда Control + E — переместит курсор в конец. Это поможет при редактировании команд.

Регистрация в GitHub

Заводим профиль в GitHub: 
1_Перейдите на сайт github.com и нажмите Sign Up
2_Пройти регистрацию 
3_ Сгенерировать SSH ключ
SSH (Secure Shell) — это протокол, который обеспечивает безопасное зашифрованное соединение между двумя устройствами через небезопасную сеть. Используется для безопасной передачи файлов.
SSH-ключ — это специальный файл; он нужен, чтобы установить безопасное соединение с другим компьютером через интернет без ввода пароля.
SSH-ключи состоят из двух частей. Одна находится у вас (это личный ключ, храните его в секрете), а вторая (публичный ключ) добавляется туда, куда вы хотите безопасно подключаться.

Генерация SSH-ключа

1_Откройте Terminal и введите команду:
ssh-keygen -t ed25519 -C "<ВАШ EMAIL при регистрации в GitHub>"

2_Дальше команда предложит:
Ввести путь до папки, где нужно сохранить ключ:
Enter file in which to save the key (/Users/practicum/.ssh/id_ed25519) 

3_Ввести парольную фразу для файла:
Enter passphrase (empty for no passphrase) 

4_Повторить парольную фразу ещё раз:
Enter same passphrase again: 

5_Выполнить команду для добавления ключа агенту 
ssh-add --apple-use-keychain ~/.ssh/id_ed25519

Добавляем SSH-ключ в GitHub аккаунт

1_Зайдите на GitHub и перейдите в Settings (Настройки).
2_В левом меню выберите SSH and GPG keys.
3_Нажмите New SSH key или Add SSH key.
4_В поле Title введите название ключа (например, название вашего компьютера).
5_В поле Key вставьте ключ из буфера обмена горячими клавишами Cmd + V.
6_Нажмите Add SSH key.


Удалённые репозитории
Создание!
1_ Открыть в терминале гит-репозиторий или создать новый
2_Перейти на страницу  github.com и нажать + рядом с иконкой профиля -> New repository
3_Заполнить название репозитория, описание, выбрть доступ и нажать Create repository.
4_Следовать инструкции github

Ветки и Pull Requests
Ветка в Git — отдельный поток разработки. В таком потоке можно безопасно пробовать новые идеи и вносить изменения не влияя на основной код проекта.
С помощью веток разработчики и разработчицы могут работать над разными задачами параллельно и сохранять основную версию проекта стабильной. Это удобно как для командной работы, так и для индивидуальных проектов, позволяет легко переключаться между разными задачами и соединять новые функции, когда они готовы.
Прежде чем писать новую функциональность, для неё нужно создать отдельную ветку.
git branch — просматриваем ветки проекта

Измените файл README.md и сделайте ещё один коммит:
echo "Изучаю работу веток" >> README.md 
git add . && git commit -m "Обновить README" 

git branch <название_ветки>: создаём ветку:
$ git brach new_branch
$ git branch # посмотрите список веток

  new_branch  # появилась новая
  * main      # * значит, мы находимся в основной ветке
  
  git checkout <название_ветки>: переключаемся между ветками: 
  
$ git checkout new_branch # перешли в новую ветку
  Switched to branch 'new_branch'

$ git branch # проверили

  * new_branch # теперь находимся тут
    main

Сливаем ветки
Перед тем как начать слияние, нужно перейти в ветку, куда должны добавиться изменения. Обычно это главная ветка. Перейдите в неё и вызовите команду git merge с именем присоединяемой ветки new_branch в качестве параметра.
$ git checkout main # переключились на главную ветку

$ git merge new_branch # объединили ветки
Updating 079cfbf..f30d441
Fast-forward
 README.md | 2 ++
 1 file changed, 2 insertions(+) 
 
 Возвращаемся в GitHub
Откройте терминал и отправьте последние изменения из основной ветки в удалённый репозиторий:
git push -u origin main

Откройте терминал и отправьте последние изменения из основной ветки в удалённый репозиторий:
git push -u origin main

Убедитесь, что вы в основной ветке. Если нет — перейдите в неё через git checkout main, а затем создайте новую ветку merge-request и перейдите в неё (git checkout -b merge-request). Откройте файл README.md и добавьте туда строку о команде git merge:
С помощью команды git merge можно слить две ветки в одну.
Закомитьте изменения git add . && git commit -m "Добавить merge в README".
Чтобы отправить merge-request в удалённый репозиторий, ещё раз выполните команду push. Теперь необязательно переходить в ветку, чтобы запушить её:
git push -u origin merge-request
Откройте GitHub и обновите страницу. После добавления новой ветки произойдёт два события:
Вместо 1 branch (англ. «одна ветка») станет 2 branches (англ. «две ветки»).
По клику на список веток теперь можно перейти в ветку feature/merge-request.


Алгоритм такой:
Вы делаете задачу в своей ветке. Когда заканчиваете работу, создаёте пулл-реквест.
Ваши коллеги проверяют, что код выглядит аккуратно, логично и работа выполнена корректно. Они могут оставить комментарии, чтобы лучше понять решение или предложить, как сделать лучше. Этот процесс называется code review (англ. «рассмотрение кода») — или просто ревью.
После финального обсуждения вы сливаете свою ветку в основную.
