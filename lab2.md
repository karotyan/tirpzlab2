## Національний технічний університет України<br>“Київський політехнічний інститут ім. Ігоря Сікорського”

## Факультет прикладної математики<br>Кафедра системного програмування і спеціалізованих комп’ютерних систем


# Лабораторна робота №2<br>"Розширена робота з git"

## КВ-21 Кукса Кирило

## Хід виконання роботи

## 1. Клонування репозиторію

### Зклонувати репозиторій для ЛР2 використавши локальний репозиторій від ЛР1 в якості "віддаленого".
```
ccuxa@DESKTOP-PG1JDDF MINGW64 ~
$ cd c:/3course/5semester/tirpz/lab2

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2
$ git clone c:/3course/5semester/tirpz/lab1/voltmeter
Cloning into 'voltmeter'...
done.

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2
```

---

## 2. Робота з ремоутами

### 2.1 Додати новий ремоут:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (main)
$ git remote add internet-origin https://github.com/karotyan/voltmeter
```

### 2.2 Показати список віддалених гілок:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (main)
$ git remote -v
internet-origin https://github.com/karotyan/voltmeter (fetch)
internet-origin https://github.com/karotyan/voltmeter (push)
origin  c:/3course/5semester/tirpz/lab1/voltmeter (fetch)
origin  c:/3course/5semester/tirpz/lab1/voltmeter (push)
```

### 2.3 Створити нову гілку та коміти:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (main)
$ git checkout -b lab2-branch
Switched to a new branch 'lab2-branch'

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add 1lab2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git commit -m "newbranch com1"
[lab2-branch 9b3c48c] newbranch com1
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1lab2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add 2lab2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git commit -m "newbranch com2"
[lab2-branch e8472f2] newbranch com2
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 2lab2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
```

### 2.4 Відправити без зв'язування:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git push origin lab2-branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 418 bytes | 418.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
To c:/3course/5semester/tirpz/lab1/voltmeter
 * [new branch]      lab2-branch -> lab2-branch
```

### 2.5 Додати коміт:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add 3lab2.txt
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git commit -m "lab2 com3"
[lab2-branch 463e822] lab2 com3
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 3lab2.txt
```

### 2.6 Відправити із зв'язуванням:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git push -u origin lab2-branch
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 232 bytes | 232.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To c:/3course/5semester/tirpz/lab1/voltmeter
   e8472f2..463e822  lab2-branch -> lab2-branch
branch 'lab2-branch' set up to track 'origin/lab2-branch'.

```

### 2.7 Додати ще коміт:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add 4lab2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git commit -m "lab2 com4"
[lab2-branch 0b3fb89] lab2 com4
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 4lab2.txt
```

### 2.8 Перевірити відправку:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 231 bytes | 231.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To c:/3course/5semester/tirpz/lab1/voltmeter
   463e822..0b3fb89  lab2-branch -> lab2-branch

```

### 2.9 Перевірити гілку у ЛР1:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ cd c:/3course/5semester/tirpz/lab1/voltmeter

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab1/voltmeter (main)
$ git branch
  lab2-branch
* main
  my-locacl-branch-2
  my-local-branch-1
```

---

## 3. Злиття гілки ЛР1 у lab2-branch:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git merge origin/my-local-branch-1 -m "merged"
Already up to date.
```

---

## 4. Перенесення комітів

### 4.1 Створити нову гілку та коміти:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (main)
$ git checkout -b lab2-branch2
Switched to a new branch 'lab2-branch2'

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git add 1lab2br2
fatal: pathspec '1lab2br2' did not match any files

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git add 1lab2br2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git commit -m "added new txt"
[lab2-branch2 b2801e5] added new txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1lab2br2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git add 2lab2br2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git commit -m "added txt"
[lab2-branch2 d71b81d] added txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 2lab2br2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git add 3lab2br2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch2)
$ git commit -m "added txt"
[lab2-branch2 9271146] added txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 3lab2br2.txt
```

### 4.2 Перенести середній коміт:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-br
$ git checkout lab2-branch
Switched to branch 'lab2-branch'
Your branch is ahead of 'origin/lab2-branch' by 2 commits.
  (use "git push" to publish your local commits)

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git cherry-pick d71b81dbf0540f4ac51720a34778f31998acbf80
[lab2-branch f5f4797] added txt
 Date: Thu Dec 26 02:56:57 2024 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 2lab2br2.txt

```

---

## 5. Визначити останнього спільного предка:
```
$ git merge-base lab2-branch lab2-branch2
9b482a1de851581a9ead10f2f52d8d797b2beb23

```

---

## 6. Робота зі сховищем (stash)

### 6.1 Зробити зміни та зберегти у сховище:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add st1.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git stash
Saved working directory and index state WIP on lab2-branch: f5f4797 added txt

```

### 6.2 Зробити ще зміни:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add st2.txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git stash
Saved working directory and index state WIP on lab2-branch: f5f4797 added txt

```

### 6.3 Відновити перші зміни:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git stash
Saved working directory and index state WIP on lab2-branch: f5f4797 added txt

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git stash apply stash@{1}
On branch lab2-branch
Your branch is ahead of 'origin/lab2-branch' by 3 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   st1.txt

```

---

## 7. Робота з `.gitignore`

### 7.1 Створити файли:


### 7.2 Додати шаблон у `.gitignore`:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git add .gitignore

ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git commit -m "added gitignore"
[lab2-branch 5d5775e] added gitignore
 2 files changed, 1 insertion(+)
 create mode 100644 .gitignore
 create mode 100644 st1.txt

```

### 7.3 Перевірити статус:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git status
On branch lab2-branch
Your branch is ahead of 'origin/lab2-branch' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

```

### 7.4 Включити ігноровані файли у статус:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git status --ignored
On branch lab2-branch
Your branch is ahead of 'origin/lab2-branch' by 4 commits.
  (use "git push" to publish your local commits)

Ignored files:
  (use "git add -f <file>..." to include in what will be committed)
        1.cust
        2.cust

nothing to commit, working tree clean

```

### 7.5 Видалити всі untracked файли:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git clean -fdx
Removing 1.cust
Removing 2.cust

```

---

## 8. Робота з `reflog`

### 8.1 Переглянути лог:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git reflog
5d5775e (HEAD -> lab2-branch) HEAD@{0}: commit: added gitignore
f5f4797 HEAD@{1}: reset: moving to HEAD
f5f4797 HEAD@{2}: reset: moving to HEAD
f5f4797 HEAD@{3}: cherry-pick: added txt
d98cad9 HEAD@{4}: checkout: moving from lab2-branch2 to lab2-branch
9271146 (lab2-branch2) HEAD@{5}: commit: added txt
d71b81d HEAD@{6}: commit: added txt
b2801e5 HEAD@{7}: commit: added new txt
9b482a1 (origin/main, origin/HEAD, main) HEAD@{8}: checkout: moving from main to
 lab2-branch2
9b482a1 (origin/main, origin/HEAD, main) HEAD@{9}: checkout: moving from lab2-br
anch to main
d98cad9 HEAD@{10}: commit (merge): hm
0b3fb89 (origin/lab2-branch) HEAD@{11}: commit: lab2 com4
463e822 HEAD@{12}: commit: lab2 com3
e8472f2 HEAD@{13}: commit: newbranch com2
9b3c48c HEAD@{14}: commit: newbranch com1
9b482a1 (origin/main, origin/HEAD, main) HEAD@{15}: checkout: moving from main t
o lab2-branch
9b482a1 (origin/main, origin/HEAD, main) HEAD@{16}: clone: from c:/3course/5seme
ster/tirpz/lab1/voltmeter
```

### 8.2 Створити нову гілку та переключитися:
```
ccuxa@DESKTOP-PG1JDDF MINGW64 /c/3course/5semester/tirpz/lab2/voltmeter (lab2-branch)
$ git checkout -b extra-branch d71b81dbf0540f4ac51720a34778f31998acbf80
Switched to a new branch 'extra-branch'

```