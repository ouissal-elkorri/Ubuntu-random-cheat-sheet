# Ubuntu-random-cheat-sheet
In this repo I will add any command I needed while working on a project or just wanted to simplify life 


## Some random commands to simplify my access to the files/folders I have

### Access a pluged phone to USB port on my laptop

Android devices usually uses the **Media Transfer Protocol (MTP)** when connecting via the USB. This protocol works **differently** than the traditional USB.

```console
username@username-laptopname:~$ cd /run/user/1000/gvfs/
username@username-laptopname:/run/user/1000/gvfs$ ls
'mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4'
username@username-laptopname:/run/user/1000/gvfs$ cd mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4
username@username-laptopname:/run/user/1000/gvfs/mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4$ ls
'Internal shared storage'  'SD card'
username@username-laptopname:/run/user/1000/gvfs/mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4$
```


ouplaaa now you can go wherever you want

---

### Open a file 

```console
username@username-laptopname:~$ xdg-open fileName
``` 
If it's a PDF it will be opened with the **Document Viewer** 
If it's a normal file it will be opened with the **Text Editor**

---
---


## Git commands

### Delete a branch remotely after a local delete
If by any accident you wanted to delete a branch(remotely & locally) but instead of **-D \<branch-name\>** you wrote **-d \<branch-name\>**, it's okay you still don't have to complicate life and use the GUI. Follow me: 

The following line will save your life

```console
username@username-laptopname:YourProjectLocation$ git push origin --delete <remote-branch-name>
```

Bingooo, check your repo

### Get the changes from the preprod or master branch to your branch
I'm working on a project with a team, each one of us pushes the changes they do to branches named after their names, for me my branch is named **ouissal**, and when anyone finishes their work they merge it to a **preprod** branch. Now I want to get the changes **from the preprod to ouissal**, here is what I did

```console
username@username-laptopname:MyProjectLocation$ git checkout preprod 
username@username-laptopname:MyProjectLocation$ git pull
username@username-laptopname:MyProjectLocation$ git checkout ouissal 
username@username-laptopname:MyProjectLocation$ git rebase ouissal preprod
```
