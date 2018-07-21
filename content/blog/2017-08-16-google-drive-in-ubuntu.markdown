---
author: rimonmostafiz
comments: true
date: 2017-08-16 22:00:00+00:00
layout: post
link: http://www.rimonmostafiz.com/google-drive-in-ubuntu/
slug: google-drive-in-ubuntu
title: Google Drive in Ubuntu
wordpress_id: 19
categories:
- technology
tags:
- google-drive
- linux
- notes
- ubuntu
---

Since there is no official Google Drive client for Ubuntu or Linux Mint but if you need to use it then there is an unofficial client called Grive2. Grive is a Google Drive client for GNU/Linux systems. It allows the synchronization of all your files on the cloud with a directory of your choice and the upload of new files to Google Drive.

Those of you used Google Drive client on Windows or Mac, Grive2 will do the same for you in Ubuntu or Linux Mint.

To install Grive2 in Ubuntu, Linux Mint and derivatives by using the main WebUpd8 PPA, use the following commands:

[bash]
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt-get update
sudo apt-get install grive
[/bash]

**Step 1: **Grive2 will download/upload new or changed files from the directory you run it. You can name it anything you want to. Let’s create a new folder – I'll create it on my _home folder and going to name it _**_GoogleDrive_**

[bash]mkdir -p ~/GoogleDrive[/bash]

**Step 2: ** Next, navigate using the terminal into the newly created “GoogleDrive” folder:

[bash]cd ~/GoogleDrive[/bash]

**Step 3: **The first time you run Grive2, you must use the “-a” argument to grant it permission to access your Google Drive:

[bash]grive -a[/bash]

After running the command above, an URL should be displayed in the terminal.
Copy that URL and paste it in a web browser. In the newly loaded page, you’ll be asked to give Grive permission to access your Google Drive and after clicking **Allow access**, an authentication code will be displayed. Copy that code and paste it in the terminal where you ran Grive2.
That’s it. Grive 2 Will start syncing your files and folder from Google Drive, wait for sync to complete for the first time. Don't close the terminal.
**
** **Now each time you want to sync Google Drive with your local _GoogleDrive_ folder, navigate to the _GoogleDrive_ folder and run grive (this time without “-a” since you’ve already authenticated Grive with Google Drive).**

If you want to sync only one sub-folder (a folder from your _~/GoogleDrive_ directory) with Google Drive, use:

[bash]grive -s folder[/bash]

(replace _folder_ with the name of the sub-folder you want to sync)

To see all the available options, type:

[bash]grive --help[/bash]

**_Courtesy:_** [_askubuntu.com_](http://askubuntu.com/)
