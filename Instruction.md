# Instruction

## Step1. Download Dropbox Uploader

Details: [www.andreafabrizi.it/2016/01/01/dropbox-uploader/](https://www.andreafabrizi.it/2016/01/01/Dropbox-Uploader/)

```shell
$ wget https://raw.github.com/andreafabrizi/Dropbox-Uploader/master/dropbox_uploader.sh
$ chmod +x dropbox_uploader.sh
```

Then directly run the script to configurate it 

```shell
$ ./dropbox_uploader.sh
```

![image-20211012183608070](C:\Users\25483\AppData\Roaming\Typora\typora-user-images\image-20211012183608070.png)

Then open https://www.dropbox.com/developers/apps.

Click "create app".

Choose an API------> Scoped access

Choose the type of access you need --------> Full Dropbox

Name your app-------> give a name 



In the "Setting" page, you can find the App Key and the App secret.

![image-20211012183928451](C:\Users\25483\AppData\Roaming\Typora\typora-user-images\image-20211012183928451.png)

Then click "Permissions" page, make sure that some following check boxes are selected,  like "files.metadata.write".

After that, open the link in terminal. (If didn't adjust the permission before open the link and get the access code, the dropbox uploader cannot work normally).

Copy and paste the access code to terminal.

Until now, the Dropbox Uploader configuration is completes.

You can use this two commands to test it.

```shell
$ ./dropbox_uploader.sh info
$ ./dropbox_uploader.sh list
$ ./dropbox_uploader.sh
```

The second one is used to list everything in the root directory. 

The third one shows the introduction of this bash script.

## Step 2. Change some details in sync script

Change the paths.

BACKUP is the folder you want to back up

TMP is a folder to store the temporary compressed files

DROPBOX is the path of dropbox_uploader.sh (which is download in Step 1)

DROPBOX_PATH is the path of corresponding Dropbox folder.



This script will automatically delete local backup files in TMP and backup files in Dropbox from up to five days ago. By changing the number of ' -5 day', you can change this setting.



