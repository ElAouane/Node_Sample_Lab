**__VAGRANT NODE-SAMPLE-APP__**
#This is a node-sample-app project for learning vagrant and linux commands.
# __Objectives Check List:__
*__Objectives_Lab_100__*
- [X] Download and install Vagrant_2.2.7_x86_64
- [X] Download and install VirtualBox-6.1.2-135663-Win
- [X] Download and install Atom or Pycharm (*Optional*)
- [ ] Swap repos with another team and test theirs to make sure the instructions are clear and all the files are included.

##### Bonus Task:
- [X] The goal is that the developers should be able to simply clone your repo and run 'vagrant up'. Can you automate the installation of the required vagrant plugins?

*__Objectives_Lab_101__*

- [X] The folder should only be accessible by the *__'Vagrant'__* user. Other users should not be able to enter the directory.

- [X] The files in the image folder have the wrong file extension. Figure out which one is correct. (Images folder was empty)

- [X] Search the manual for a command that will help you to rename multiple files at once

- [X] The four files called puppy are an old format and need to be deleted. Try to delete them with a single command.

- [X] He says there was a file called `index.html` that he tried to rename but it disappeared. Try to find it and fix it.

- [X] The file are going to be public. The owner needs full permissions but the group only need to be able read to the files.

**Installation**

**Step 1:**

To accomplish and build a healthy and working DevOps environment we need to download some software to help us to build a Virtual Machine where we can upload and test our project. The best choice it is to set a linux operative system Ubuntu on a Virtual Machine.

Lets start: Visit the website:

````
https://www.vagrantup.com/downloads.html
````
Download the Windows version:


*Vagrant Definition:*

`
Vagrant is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.
`
Once the download has been completed, please start the installation and follow the installation wizard. When the installation has been terminated, you will be asked to reboot your computer, say no and lets move through our next step.

**Step 2:**

Once we have completed out Vagrant software, we need to proceed and download and install another important tool which will help us and define further more our project.

Visit the website and Download VirtualBox:

`https://www.virtualbox.org/wiki/Downloads`

In the Top of the page you will be offered 4 different linked based on which operative system you are working.

1. Windows Hosts
2. OS X Hosts
3. Linux Distributions
4. Solaris Hosts

As we are working on a windows machine, we proceed and download and install Windows Hosts.
After the download start the installation process. At the end you will be asked to reboot your computer...what will you reply?......wrong, this time say yes and reboot :joy:

**_IMPORTANT:_**  If during the VirtualBox installation you will encounter an error. Don't panic, probably you never had any container software installed before so you windows cache doesnt containt any information about how to link together your Vagrant (installed earlier) and your VirtualBox. Close the installation prompt(Virtual Box) and reboot your computer. This will allow windows to fully check and cache the data regarding your Vagrant installation and link it to VirtualBox. We are almost set :heart_eyes: , complete your Virtual box installation.

**But what is VirtualBox and why do we need it?**

`Oracle VM VirtualBox enables you to run more than one OS at a time. This way, you can run software written for one OS on another, such as Windows software on Linux or a Mac, without having to reboot to use it`

**Step 3:(_Optional_)**

Developer likes to show off, and we are not less :persevere:
During the process of set up of our Virtual MAchine and Container, we will need to manually configure some file, and a easy way to do so is using a IDE (*Integrated Development Kit*). Those Software are use because privides comprehensive facilities to computer programmers for software development.

For this course and tutorial, you can download Atom, a free software that you can download at

`https://atom.io/`


**Step 4:**
We made it untill here safe :sunglasses:

Lets create a folder where we can start working. In my case a choose `Documents` Folder. Open you `git bash` and navigate untill the Folder you have created.

Let go to github and start cloning out repository. But to follow step by step this tutorial, we need to Fork a third party repo so we can carry on our objectives, solve our task and be a good DevOps :eyes:

Go to:
`https://github.com/spartaglobal/node-sample-app`

Most likely you will encounter on github repositories where the owner does not allow any commit or push. But still, this will not stop us. Github offers the option to Fork somebody else repository.
Fork :yum:

What does Fork mean in this scenario, simply mean we can create a perfect copy of that repository and transfer it to our repository list, this will allow us to start working and developing our code starting for that master timeline and we can commit , push, delete without asking permission to anybody. So lets do it.
On the link provided, on the *TOP* *RIGHT* side of the page you will find a Fork button, looks safe and nice...PRESS IT!!!
This will take a few moments, as github is providing a full copy of the repo in your list. At the end of the process go to you repo and open the Node-Sample-add.
Green button on the *RIGHT*: looks safe, press it and copy the link.
We are done for now with git.

Got to the folder that you created earlier Create a folder inside (named as you wish) and open gitbash in that location.

**Beatifull!!**

Now in the console, type
`Git clone` and paste the link copied and press enter.
And now magic will happen. Gitbash will connect to your repository, get the repo provided in that link and download it in you folder.


# Run Vagrant

Once gitbash finished cloning your repo, go back to the main folder by using gitbash command `cd` or just use the back arrow. Just make sure that you are in the root folder.


#Set up Vagrant.
Before to start setting up our safe zone (Enviroment Virtual Machine) lets take a look to the following website:

`https://app.vagrantup.com/boxes/search`

Here we can find the full collection of images, virtualboxes, vmware and much more.
If you click on virtualbox and you type `Ubuntu Bionic` you can see a list of different ubuntu images, with some details about download and release.
For our purpose, we are gonna use the ufficial Ubuntu `Ubuntu/bionic64`

Without further ado lets head back to out gitbash, and type:

`vagrant init ubuntu/bionic64`

This simple command, will run the vagrant API, look in his metadata for ubuntu/bionic64, and if is not in our system, it will start 'initializing' a copy for us downloading `.vagrant` folder and a `vagrantfile` config file. This process will take a while.

**Nice** our Vagrant is set up and we can run it.

If you open now your VirtualBox, you will find a VirtualMachine in it, ready to take off. Lets do it!!

In the same gitbash.

Type:

`Vagrant up`

Simple command to say we want to go on with our virtual machine.
Simple command but in the background runs some important step. Such as setting the VM and the `image` required,`clear previous network interface`, `Forwarding ports` creating a `SSH` key, and checking `vagrantfile` and its config.
But for now, the most **important** for us, it that it will start smothly and without errors :joy:

Lets wait untill it finish loading all the setup and lets pay attention and go in details on the `SSH` key.

`SSH`: SSH is a Secure Shell password, a software package that enables secure system administration and file transfer over insecure network. The SSH protocol uses encryption to secure the connection between clients and a server. But Lets focus on out `STDOUT` where is state that the key is insecure ad is setting a new one.
Mainly, when we are starting up our vagrant, the software need to generate quickly a SSH key to have full access to the file to runs, once this `job` has been accomplished, and he used a standard key, to prevent future problem and using the "power" that has in that momemt, it provide a `NEW` and unique key for us.

Lets dive in our Vagrant VM now.

Type `vagrant ssh`

**UPDATE AND UPGRADE**
Once the Vagrant ssh has loaded all the setting, we need to update and upgrade all the files and drivers. as the VM might be out of date.

first thing first lets run:

`sudo apt-get update` and press enter:

(*IMPORTANT:* sudo is a keywprd which replicate the super uder power for the current user without changing his permissions)

`sudo apt-get upgrade -y`

upgrade the software `-y` stand for `Yes, confirm..install everything`

PErfect, ready for the serious stuff now.

To be able to run our project, we need a tool which allow us to replicate a database, and for this purpose we are gonna use nginx:

`sudo apt install nginx`

if does prompt if you want to proceed, type `y` and enter.

Once is done lets start the nginx process

`sudo systemctl start nginx`.

# **__We are done with the settings finally__**


#### Task:The folder should only be accessible by the `vagrant` user. Other users should not be able to enter the directory:

- To complete this task we need to go back to out folder where we cloned the  our repo and open our `vagrantfile`, now we have to sync our VM with our Hosts.

```
config.vm.synced_folder "./node-sample-app", "/home/vagrant/node-sample-app",
  owner: 'vagrant'
```

The first Quotetion, refere to the folder on our host machine, we we are actually running windows, and the second bit refer to our VM machine. Usually those two folder matches and allow us to sync every single changes on both ends and mirror them on the opposit end.
Us constrait i added `OWNER` which refers to vagrant user. In fact, doing so, if i change user to `root` I wont be able to see node-Sample-App.. but if i go back to vagrant user, i can see it and access it

How to change user:

`sudo -u root`
or if you are in root and want to go to vagrant

`sudo -u vagrant`

If while changing user asks you for a password.. the default password should be `vagrant`

#### Task: Search the manual for a command that will help you to rename multiple files at once


#### Task: He says there was a file called index.html that he tried to rename but it disappeared. Try to find it and fix it.
through the shell navigate to the location of the index.ejs and Type:
`index.ejs` and as a STDOUT will tell you that is a HTML..go to the folder and rename the file to `index.html`


#### Task: The file are going to be public. The owner needs full permissions but the group only need to be able read to the files.

Based on recent documentation, apprently Windows itself stated that they are not allowed to go deep on WSL to change the permission right on a Virtual MAchine, there are 2 option, one useless and one risky.

Useless: go on your host machine and from the property of the file or directory change the permissions.

Risky: from your `vagrantfile`, add the string command

`  config.vm.synced_folder "./node-sample-app", "/home/vagrant/node-sample-app",
    owner: 'vagrant',
    group: 'root',
    mount_options: ["dmode=444" , "fmode=444"]`

Accessing the file configuration everytime, on the long run, it might break the vm or change something that it might affect our VM performance, but why i set on the ruby code is simple.
For the mount option `dmode` stands for Directory Mode, or what permission would you like to user for all users, and fmode stands for File mode and what permission to it.

Changing the permissions code, will affect the permission access for all the users.

On the same documentation I was consulting, I read that the chmod as we know it on linux ubuntu, it might be working without any problem.
