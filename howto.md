
PS C:\Users\kuuzi\IdeaProjects\github> git init
Reinitialized existing Git repository in C:/Users/kuuzi/IdeaProjects/github/.git/
PS C:\Users\kuuzi\IdeaProjects\github>
PS C:\Users\kuuzi\IdeaProjects\github> git remote add upstream-my https://github.com/kuzichevapd/KotlinAsFirst2021
PS C:\Users\kuuzi\IdeaProjects\github> get fetch
get : Имя "get" не распознано как имя командлета, функции, файла сценария или выполняемой программы. Проверьте правильность написания имени, а также наличие и правильность пути, после
чего повторите попытку.
строка:1 знак:1
+ get fetch
+ ~~~
    + CategoryInfo          : ObjectNotFound: (get:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\kuuzi\IdeaProjects\github> git fetch
PS C:\Users\kuuzi\IdeaProjects\github> git fetch upstream-my
remote: Enumerating objects: 563, done.
remote: Counting objects: 100% (76/76), done.

Receiving objects: 100% (563/563), 177.43 KiB | 440.00 KiB/s, done.
Resolving deltas: 100% (277/277), completed with 16 local objects.
From https://github.com/kuzichevapd/KotlinAsFirst2021
* [new branch]      master     -> upstream-my/master
  PS C:\Users\kuuzi\IdeaProjects\github> git rebase --onto master 1137b420cc95fa6894edad69b31e2da1bb985d1d upstream-my/master
  Successfully rebased and updated detached HEAD.
  PS C:\Users\kuuzi\IdeaProjects\github> git branch backport
  PS C:\Users\kuuzi\IdeaProjects\github> git checkout master
  Previous HEAD position was 4427554 7
  Switched to branch 'master'
  Your branch is up to date with 'origin/master'.
  PS C:\Users\kuuzi\IdeaProjects\github> git merge backport
  Updating d535f35..4427554
  Fast-forward
  input/center_in1.txt          |   7 --
  pom.xml                       |   8 ++
  src/lesson1/task1/Simple.kt   |  19 +--
  src/lesson2/task1/IfElse.kt   |  69 ++++++++++-
  src/lesson2/task2/Logical.kt  |  36 +++++-
  src/lesson3/task1/Loop.kt     | 148 +++++++++++++++++++++--
  src/lesson4/task1/List.kt     | 121 +++++++++++++++++--
  src/lesson5/task1/Map.kt      |  38 ++++--
  src/lesson6/task1/Parse.kt    | 114 ++++++++++++++++--
  src/lesson7/task1/Files.kt    | 271 +++++++++++++++++++++++++++++-------------
  src/lesson8/task1/Geometry.kt |  63 +++++++++-
  src/lesson8/task2/Chess.kt    |  88 +++++++++++++-
  test/lesson4/task1/Tests.kt   |   2 +-
  test/lesson5/task1/Tests.kt   |   5 +
  test/lesson6/task1/Tests.kt   |  10 +-
  test/lesson7/task1/Tests.kt   |  13 ++
  16 files changed, 850 insertions(+), 162 deletions(-)
  PS C:\Users\kuuzi\IdeaProjects\github> git remote add upstream-theirs https://github.com/pavelminin2002/KotlinAsFirst2021
  PS C:\Users\kuuzi\IdeaProjects\github> git fetch upstream-theirs
  remote: Enumerating objects: 277, done.
  remote: Counting objects: 100% (94/94), done.
  Receiving objects: 100% (277/277), 38.56 KiB | 1.84 MiB/s, done.183Receiving objects:  90% (250/277)
  Resolving deltas:   8% (11/131)
  Resolving deltas: 100% (131/131), completed with 11 local objects.
  From https://github.com/pavelminin2002/KotlinAsFirst2021
* [new branch]      master     -> upstream-theirs/master
  PS C:\Users\kuuzi\IdeaProjects\github> git merge -s ours upstream-theirs/master
  Merge made by the 'ours' strategy.
  PS C:\Users\kuuzi\IdeaProjects\github> git remote -v > remotes
  PS C:\Users\kuuzi\IdeaProjects\github> git add remotes
  PS C:\Users\kuuzi\IdeaProjects\github> git commit -m "Add remotes file"
  [master 969269e] Add remotes file
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 remotes
