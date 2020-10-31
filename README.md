# kottans-frontend
In this repository I will write about the work with which I dealt and I will write reports on the lessons I have learned, so have fun (smile)

![img](img-readme/1_J8O2xd9ZqxWr2x6EP4MHmg.png)

## Notes

---
### General
---

- [X] *0. [Markdown](#markdown)*
- [X] *1. [Git Basics](#git)*
   - [X] *1.1 [Version Control with Git](#version)*
   - [X] *1.2 [learngitbranching.js.org](#learngit)*
- [X] *2. [Linux CLI and Networking](#linux)*
- [X] *3. [VCS (hello gitty), GitHub and Collaboration](#github)*

---
### Front-End Basics
---

- [X] *4. [Intro to HTML & CSS](#markdown)*
- [X] *5. [Responsive Web Design](#markdown)*
- [ ] *6. [HTML & CSS Practice](#markdown)*
- [ ] *7. [JavaScript Basics](#markdown)*
- [ ] *8. [Document Object Model](#markdown) - practice*

---
---
   
## Markdown

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

![img](git_basics/VCS.png)

----

> Git is a free and open source distributed version control system designed 
>> to handle everything from small to very large projects 
>>> with speed and efficiency.

----

***My expectations from [course about Git](https://classroom.udacity.com/courses/ud123)***: I didn't know what to expact, besause before that I had no idea what is Git and what is he like (forgive me Mark Zuckerberg).

---

Let's break everything down:

- As soon as I have started lerning course and generelly found out what's version control system - I was very suprised. Exactly from that we use this system, I, and almost every   user use it for a long time and even didn't notice it. What I'm talking about? Do you know about this key combination as `ctrl + z`? Do you know what this key combination do?   It's used to undo the last action (for examle, to deletion text (i think you alredy knew it)).

  - Moreover this only a small part of version control system.

 - Then I had a difficult time for exposition terminology, here are some points:
   - Repository/repo: storage for storing your works (files), and few files, which are used for collaboration with Git.
   - A version control system (abbreviated as VCS) this is tool with which you can manage version control.
   - Branch - creation new branch for you repo in which you can safely change file that you need without touching a main branch.
     - Also you can merge branches, but let's speek about it a little bit later.
    
- After that installation Git on Windows, nothing complicated, everything okay.

- Further, at every lesson I have learnt different commands, similiarly i will sort this commands in different blocks.

---

#### Lesson 2: Create A Git Repo

   | Command | What is it mean? |
   | --- | --- |
   | `git init` | Create brand new repositories |
   | `git clone` | Copy existing repo from somewhere else to your local computer |
   | `git status` | Check the status of a repo |
    
- And the most important detail: ***always, hear, always*** use command `git status`.

---

#### Lesson 3: Review a Repo's History

   | Command | What is it mean? |
   | --- | --- |
   | `git log` | Displays information about the existing commits |
   | ~~Showing how the terminal looks like~~ | ![img](img-readme/Screenshot_44.png) |
   | `git show` | Dislays information about just that one commit |
   | Typically, a SHA is provided as a final argumen | ![img](img-readme/Screenshot_45.png) |
 
 - When do we use the command `git log`, terminal outputs to us all available information: abous SHA, about author, date when was made last change and commit. What if we only      want to see SHA and commit, what if we need to show just the only line? For this we can use ***flag***. Flags could used for changing program work or changing display this      or that command in terminal.
   - For example, `git log --oneline` displayed just the short SHA and the commit message in one line.
   - The `git log` command has a flag that can be used to display the files that have been changed in the commit, as well as the number of lines that have been added or               deleted. The flag is `--stat`.
   - `git log` has one more comman, which shows **where ___exactly___*** was produced change file. This command is named `--patch`, but nobody wants to write constantly `--        patch`, because of that you can use this command like `git log -p`.
   
---

#### Lesson 4: Add Commit To A Repo

   | Command | What is it mean? |
   | --- | --- |
   | `git add` | Add files from the WD to the SI |
   | `git commit` | Take files from the SI and save them in the repo |
   | `git diff` | Displays the difference between two version of a file |
   
  - That not to use `git add` separately for each file, there is a more simplified way. Period(.). Yeah, you just add `.` to `git add` (not forgetting to make a space between      these commands). Trully be carefull, don't add wrong file to SI.
   - If such situation happend, so return unplanned added file to WD, add to your project file `.gitignore` and add everything unnecessary to this file (photos, documents,           fonts, everithing you don't need to work with in terminal). 
   
  - You can write commit in terminal using flag `-m`, in this way you get command `git commit -m "Justi commit, nothing more"`.
  - `git diff` command can be used to see changes that have been made but haven't been committed, yet.
  
---

#### Lesson 5: Tagging, Branching, and Merging

   | Command | What is it mean? |
   | --- | --- |
   | `git tag` | Add tags to specific commits |
   | `git branch` | Allows multiple lines of development |
   | `git checkout` | Switch between different branches and tags | 
   | `git merge` | Combines changes on different branches |
   
   - The `git branch` command is used to:
     - list all branch names in the repository
     - create new branches
     - delete branches
     
---

#### Lesson 6: Undoing Changes 

   | Command | What is it mean? |
   | --- | --- |
   | `git commit --amend` | Alter the most-recent commit |
   | `git revert SHA` | Reverses given commit |
   | `git reset` | Erases commit | 
   
   - `git reset` is the most ***powerfull*** command in Git. You can help or hurt yourself. Occasionally you can delete last commit or all branch. Be carefull with this command.
   
---
---

***IN CONCLUSION***: I'm so glad that i finished this couse, I received a lot of knowledge, which ***100%*** will using in the future. I was shocked because of documentation on the English language I  know English quite well but was without practic so long time. It was difficult at start, don't deny, I even find friendship with my vocabulary book, but move ahead and ahead I can say with all confidence, that it is already clearly in english.

Yeah, about course. So surprised Git with itself Version Contol System, suprised, that you can work in moment in different branches parallel to each other nothing occasionally didn't change, surprised that you can come back in needed for you commit in all time. Everything is so interesting and I will be learning this (and using).

---
---

#### Dictionary of abbreviations

_**WD** - Working Directory_

_**SI** - Staging Index_

---

## learngitbranching.js.org

![img](git_basics/Screenshot_48.png)

![img](git_basics/Screenshot_49.png)

---

In this couse, I against (like always) have shocked by English? What, English? Allright, because now it was harder maybe in three times, really. But I didn't despair and go ahead to my target! So, right in these course I did't find so many commands like in last times, but anyway it was (I am talking about new commands). 

For exapmle, i understood the remote repo much better then in previous time, so good that in these course they are used a demo for demonstrate how it's work.

Anyway, I will be going to use Git in future project, so let's move on.

---
---

***IN CONCLUSION***: learn new commands, found a new experience in using Git!!!

---
---

## Linux CLI, and HTTP

![gif](task_linux_cli/linux.gif)

Okay, I did it against. I finished one more course and I so proud for myself. I learnt what Linux is made of and what it is. It's not like Windows, not even close. It's like... something different, which I didn't see before, something new (of course for me, because I'm using Windows).

But, forgetly all words above, It looks a bit like Git, I found similar commands. In all, I would be learn about Linux in future and maybe and install myself as an operating system.

---
---

***IN CONCLUSION***: I learnt new operating system. Wow. Okay, just started learning, but that's one small step for programming, one giant leap for me.

---
---

P.s. Why did I stop writing about my study? Why did I stop making tables, inserting screenshots from courses to show what this or that program does? It takes so much time and I don't have time to study. Therefore, of two things I had to choose the one that I want to spend more time to, and that is study!

---

## Git Collaboration

![img](task_git_collaboration/Screenshot_71.png)

Oh, hello! I have already finished one more course about Git.

***My expectations from [course about Git](https://classroom.udacity.com/courses/ud123)***(*against*): I wanted to learn how to work on remote repo, (*spoiler*) I have got it.
What I have learnt from this course?
1. Working with remote repo.
   - Now I knew how to create a remote repo - `git remote`.
   - How to work correctly with GitHub.
   - How to connect remote repo with local - `git remote add origin http://...`.
   - `git push` - push local repo to remote.
   - `git pull` - get commit from remote repo to local.
   - `git fetch` - get commit from remote repo to local and don't merge.
2. Working on another developer's repo.
   - Fork in GitHub isn't noun - it's a verb.
   - Git haven't command git fork, so do fork in GitHub.
   - `git log --author=Surma` find commit from author Surma using `git log using flag --author`.
   - Discover how many comments left author - `git shortlog -s -n`.
   - Find commit using keyword - `git log --grep=keyword`.
   - Discover what I must to do before doing pull request.
3. Staying in sync with a remote repo.
   - How to create pull request.
   - Manage an active PR.
   - Squash commits with command `git rebase`.
   
---

![img](task_git_collaboration/Screenshot_48.png)

![img](task_git_collaboration/Screenshot_49.png)

I have nothing to add, completed this task couple days ago.

---
---

***IN CONCLUSION***: Okay, it's all with Git. Of course I will use all this recommandations and will using all commands from this big course.

---
---

#### Dictionary of abbreviations

_**PL** - pull request._

---

## Intro to HTML and CSS

![img](task_html_css_intro/Screenshot_72.png)

***My expectations from [course "Intro to HTML & CSS (Eng)"](https://classroom.udacity.com/courses/ud001)***: I have no expactations, because I already had known this material before started this course.

Be good, that I repeated part of command and tools from html and css.

---

![gif](task_html_css_intro/learn_html_css.gif)

***My expectations from [course "Learn HTML(Eng)"](https://www.codecademy.com/learn/learn-html) and [course "Learn CSS(Eng)"](https://www.codecademy.com/learn/learn-css)***: I didn't wait something new for me, because I already did some websites and know how to use html and css.

---
---

***IN CONCLUSION***: Once again, I knew everything from these courses before, so now it was just  practice of all my knowledges

---
---

## Responsive Web Design

![img](task_responsive_web_design/Screenshot_78.png)


***My expectations from [course "Responsive Web Design Fundamentals"](https://www.udacity.com/course/responsive-web-design-fundamentals--ud893)***: I wanted understood responsive web design and this course gave me a boost for start to do it.

---

![img](task_responsive_web_design/Screenshot_80.png)

***My expectations from [game "Flexbox Froggy"](http://flexboxfroggy.com/#ru)***: I have already deal with this game.

---
---

***IN CONCLUSION***: Generally, I knew some things before starting this course, like 
``<meta name="viewport" content="width=device-width, initial-scale=1.0">`` or media queries, but in this course I improved my knowledges. What about the game "flexbox froggy"? I have already completed this game in the past, so against - nothing new.

---
---

## HTML/CSS-practice

<a href="https://smillims.github.io/html-css-popup/"><img src="task_html_css_practice/Screenshot_79.png" alt="Screenshot" style="cursor: pointer;"></a>

*Click above to open website*

***My expectations from HTML/CSS-practice***: Oh, it should be... hard.

And yeah, it was a little hard :grin:

---

**What was the most hardest for me?**

1. I can't understood how to open menu without JavaScript. Yeah, for whole first day I had just add background-image, wrote navbar in html, stylized it in css and thinked how to open menu with html helping. Tried to find the answer but almost everywhere was written somethink like "In JavaScript ...".

2. So the next day I have still searching answer. But in this time luck turned back to me. So I used combination something like `click here ~ open here`. After that, I have finished navbar, I have complited the rest part of my work.

---
---

***IN CONCLUSION***: Now, I understand more how to interact with html coding.

---
---
