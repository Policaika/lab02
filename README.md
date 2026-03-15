Part I

1) Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).

- [x]

2) Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.

…or create a new repository on the command line

echo "# lab02" >> README.md
- [x] git init
- [x] git add README.md
- [x] git commit -m "first commit"
- [x] git remote add origin https://github.com/Policaika/lab02test.git
- [x] git push -u origin main


┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git init              
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
hint:
hint: Disable this message with "git config set advice.defaultBranchName false"
Инициализирован пустой репозиторий Git в /home/p/Рабочий стол/Policaika/workspace/reports/lab02/.git/

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git add README.md 

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git status       
Текущая ветка: master

Еще нет коммитов

Изменения, которые будут включены в коммит:
  (используйте «git rm --cached <файл>...», чтобы убрать из индекса)
        новый файл:    README.md

Неотслеживаемые файлы:
  (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
        .README.md.swp

Для того, чтобы временный файл с раширение .swp, то есть чтобы так называемые dump-files не мусорили репозиторий, создадим файл с расширением .gitignore - те файлы,
которые не будут попадать в репозиторий, а затем добавим туда исключаний. Все это нужно для того, чтобы не добавлять каждый раз через git add конкретный файл, а добавить всю
директорию сразу: git add .

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ touch .gitignore

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ cat .gitignore 
*build*/
*install*/
*.swp
.idea/

После этого видим такую картину

──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git add .        
                                                                                                                                                                                   
┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git status
Текущая ветка: master

Еще нет коммитов

Изменения, которые будут включены в коммит:
  (используйте «git rm --cached <файл>...», чтобы убрать из индекса)
        новый файл:    .gitignore
        новый файл:    README.md

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git commit -m "first commit"  
[master (корневой коммит) df6b965] first commit
 2 files changed, 47 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md

┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git remote add origin https://github.com/Policaika/lab02.git
                                                                                                                                                                                   
┌──(p㉿Policai)-[~/…/Policaika/workspace/reports/lab02]
└─$ git remote -v                                               
origin  https://github.com/Policaika/lab02.git (fetch)
origin  https://github.com/Policaika/lab02.git (push)



3) Создайте файл hello_…or create a new repository on the command line
Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.
4) Добавьте этот файл в локальную копию репозитория.
5) Закоммитьте изменения с осмысленным сообщением.
6) Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.
7) Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?
8) Запуште изменения в удалёный репозиторий.
9) Проверьте, что история коммитов доступна в удалёный репозитории.

Part II

Note: Работать продолжайте с теми же репоззиториями, что и в первой части задания.

10) В локальной копии репозитория создайте локальную ветку patch1.
11) Внесите изменения в ветке patch1 по исправлению кода и избавления от using namespace std;.
12) commit, push локальную ветку в удалённый репозиторий.
13) Проверьте, что ветка patch1 доступна в удалёный репозитории.
14) Создайте pull-request patch1 -> master.
15) В локальной копии в ветке patch1 добавьте в исходный код комментарии.
16) commit, push.
17) Проверьте, что новые изменения есть в созданном на шаге 5 pull-request
18) В удалённый репозитории выполните слияние PR patch1 -> master и удалите ветку patch1 в удаленном репозитории.
19) Локально выполните pull.
20) С помощью команды git log просмотрите историю в локальной версии ветки master.
21) Удалите локальную ветку patch1.

Part III

Note: Работать продолжайте с теми же репоззиториями, что и в первой части задания.

22) Создайте новую локальную ветку patch2.
23) Измените code style с помощью утилиты clang-format. Например, используя опцию -style=Mozilla.
24) commit, push, создайте pull-request patch2 -> master.
25) В ветке master в удаленном репозитории измените комментарии, например, расставьте знаки препинания, переведите комментарии на другой язык.
26) Убедитесь, что в pull-request появились конфликтны.
27) Для этого локально выполните pull + rebase (точную последовательность команд, следует узнать самостоятельно). Исправьте конфликты.
28) Сделайте force push в ветку patch2
29) Убедитель, что в pull-request пропали конфликтны.
30) Вмержите pull-request patch2 -> master.
