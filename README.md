# Ubuntu-random-cheat-sheet
In this repo I will add any command I needed while working on a project or just wanted to simplify life 


## Some random commands to simplify my access to the files/folders I have

### Access a pluged phone to USB port on my laptop

Android devices usually uses the **Media Transfer Protocol (MTP)** when connecting via the USB. This protocol works **differently** than the traditional USB.

1.
```console
username@username-laptopname:~$ cd /run/user/1000/gvfs/
username@username-laptopname:/run/user/1000/gvfs$ ls
'mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4'
username@username-laptopname:/run/user/1000/gvfs$ cd mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4
username@username-laptopname:/run/user/1000/gvfs/mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4$ ls
'Internal shared storage'  'SD card'
username@username-laptopname:/run/user/1000/gvfs/mtp:host=OPPO_CPH1909_Z9UCWOFUFM69HYT4$
```


#ouplaaa now you can go wherever you want

