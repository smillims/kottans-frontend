# kottans-frontend
In this repository I will write about the work with which I dealt and I will write reports on the lessons I have learned, so have fun (smile)
## Notes

- [X] *0. [Formatting](#)*
- [ ] *1. [Git Basics](#)*
   - [ ] *1.1 [Version Control with Git](#)*
   
## Formatting

   The first innovation that I have discovered for myself is that you need to use **markdown** formatting to edit text, and what's even funnier is that you need to style everything ***with your own hands***, without using pre-prepared buttons.

---

1. From the very beginning, everything was difficult and unusual, but after sitting and studying the information for two days I can say, that this is not such a difficult topic for me. Now I'm going to show you (and remind myself) some commands, each of which fulfills different functions.

- For examle you can stylized your own **header**:
   
   | Symbol | Heading text |
   | :--- | :---: |
   | `#` | Like `h1` header |
   | `###` | Like `h3` header |
   
   - and etc., when end at six `#` symblols

---

2. To your attantion I want to present command with which you're be able to use ordered/unordered **lists**. Above you can see example unordered lists. But from below will already be presented commands for created list:

```
- Kottans
- Front-end
- Course
```
- Kottans
- Front-end
- Course

```
1. Git
2. is a distributed
3. version-control system
```

1. Git
2. is a distributed
3. version-control system

---

3. Okay, let's move. Further I was shoked by creating **table**. Not the table itself, no no :grin:, specifically ***table creation***, I'll show you now:

   ```
   | HTML | CSS | JavaScript | Python |
   | --- | --- | --- | --- |
   | :heavy_check_mark: | :heavy_check_mark: | :x: | :x: |
   ```

   | HTML | CSS | JavaScript | Python |
   | --- | --- | --- | --- |
   | :heavy_check_mark: | :heavy_check_mark: | :x: | :x: |

   - The table shows the markup and program languages which I use/not use

---
---

***IN CONCLUSION***: Yeah, generally markdown it's basic, but in all that's information was new for me. I spent some of my time on learning, because of that I should to write about it here. On the whole, finishing. In notes I described just a little part of all, that I had to find out, not to mention stylized text (by the way, which I'm using), about code blocks (which I use too ! ), emogi, [design elements](https://shields.io/) and few different items.

---
---

## Git Basics
### Version Control with Git

----

> Git is a free and open source distributed version control system designed 
>> to handle everything from small to very large projects 
>>> with speed and efficiency.

----

***Мои ожидания от [курса по git](https://classroom.udacity.com/courses/ud123)***: я не знал чего ожидать, потому до этого даже понятия не имел что такое git и что он из себя представляет (да простит меня Марк Цукерберг).

---

Разложим все по пунктикам:

- Как только я начал проходить курс и вообще узнал что такое система контроля версий - я сильно удивился. А именно с того, что эту систему я, да и почтый каждый пользователь       используем уже давно и даже не замечаем этого! О чем я говорю? Вкурсе о таком сочитании клавиш как `ctrl + z`? А вкурсе что делает это сочетание клавиш? Оно используется для     отмены последнего совершенного действия (например, удаления текста (думаю вы и так это знали)).

  - Причем это только малая часть контроля версий

- Дальше мне предстояла трудная пора для разжовывания терминологии, вот несколько пунктиков:
  - Repository/repo: хранилище для хранения своих работ (файлов), а также несколько файлов, которые используются для связи с Git.
  - A version control system (abbreviated as VCS) это инструмент с помощью которого можно управлять контролем версий.
  - Branch - это создание новой ветки в твоем репозитории в которой ты можешь безопасно изменить нужный тебе файл не затрагивая при это основную ветку.
    - Также ветки можно соединить, но об этом уже немного позже.
    
- Потом установка Git на Windows 7, ничего сложного, все окей.

- Дальше на каждом уроке я изучал разные команды, так же в разные блоки буду их и сортировать.

---

#### Lesson 2: Create A Git Repo

   | Command | What is it mean? |
   | --- | --- |
   | `git init` | Create brand new repositories |
   | `git clone` | Copy existing repo from somewhere else to your local computer |
   | `git status` | Check the status of a repo |
    
- И самая главная деталь: ***всегда, слышишь, всегда*** используй команду `git status`.

---

#### Lesson 3: Review a Repo's History

   | Command | What is it mean? |
   | --- | --- |
   | `git log` | Displays information about the existing commits |
   | ~~Показываю как выглядит терминал при вписании команды~~| ![img](img-readme/Screenshot_44.png) |
   | `git show` | Dislays information about just that one commit |
   | Typically, a SHA is provided as a final argumen | ![img](img-readme/Screenshot_45.png) |

 - Когда мы испольльзуем команду `git log`, то консоль выводит нам всю имеющуюся информацию: про SHA, про автора, дату когда было внесено последнее изменение и сам commit. А        вдруг мы хотим увидеть только SHA and commit, вдруг нам надо воспроизвести все в одну линию? Для этого мы можем использовать ***flag***. Flag ипользуют для изменения функции    или видоотбражения, с помощью которой вписывают определенную команду к уже существующей команде.

   - К примеру, `git log --oneline` displayed just the short SHA and the commit message in one line.
   - The `git log` command has a flag that can be used to display the files that have been changed in the commit, as well as the number of lines that have been added or deleted.     The flag is `--stat`.
   - `git log` имеет еще одну команду, которая показывает **в каком ___именно___ месте** была произведина измена файла. И это команда имеет название `--patch`, но никто не хочет     постоянно писать `--patch`, поэтому *бараманная дробь* можете использовать эту команду так - `git log -p`.
   
---

#### Lesson 4: Add Commit To A Repo

   | Command | What is it mean? |
   | --- | --- |
   | `git add` | Add files from the WD to the SI |
   | `git commit` | Take files from the SI and save them in the repo |
   | `git diff` | Displays the difference between two version of a file |

  - Чтобы не использовать `git add` отдельно к каждому файлу, есть более упрощенный способ. Period(.). Да, ты просто добавляешь `.` к `git add` (не забывая делать пробел между      этими командами). Правда буть осторожен, не добавь не тот файл в SI.
   - Если уж получилась такая беда, то верни незаплонированно добавленный файл в WD, добавь в свой проект файл `.gitignore` и уже в этот файл добавь все лишнее (фотографии,         документы, шрифты, все с чем тебе не понадобится работать в терминале).
   
  - Ты сразу можешь написать commit в терминале используя flag `-m`, так у тебя получится команда `git commit -m "Justi commit, nothing more"`
  - `git diff` command can be used to see changes that have been made but haven't been committed, yet.

---

#### Lesson 5: Tagging, Branching, and Merging

   | Command | What is it mean? |
   | --- | --- |
   | `git tag` | Add tags to specific commits |
   | `git branch` | Allows multiple lines of development |
   | `git checkout` | Switch between different branches and tags | 
   | `git merge` | Combines changes on different branches |

#### Словарь сокращений

_**WD** - Working Directory_

_**SI** - Staging Index_
















