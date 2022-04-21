# **Lab One Report**
---
## *1. Installing VScode*
![Image](https://dwengxz.github.io/cse15l-lab-reports/1.png)
* download VScode for your operating system from [the VScode website](https://code.visualstudio.com/download)
* depending on the version, the starting screen will vary, but should look similar to the screenshot above

## *2. Remotely Connecting*
![Image](https://dwengxz.github.io/cse15l-lab-reports/2.png)
* remotely connect to the remote host with the following command, replacing 'zz' with your account-specific letters

```$ ssh cs15lsp22zz@iengy6.ucsd.edu```
* you will be prompted to enter your password; type in your password (it will look like nothing is being typed, but it is) to finish connecting
* results should look similar to the screenshot above

## *3. Trying Some Commands*
![Image](https://dwengxz.github.io/cse15l-lab-reports/3.png)
* using some of the provided git commands below, familiarize yourself with using git
```
cd - navigates to a new directory
ls - lists the files within the provided directory 
pwd - prints the path to the current directory
mkdir - makes a new directory
cp - copies a given file/directory to a new location
touch - creates a file with a given name
rm - deletes the given file/directory
```
* in the above screenshot, I decided to use `ls`, `touch`, and `rm`

## *4. Moving Files with `scp`*
![Image](https://dwengxz.github.io/cse15l-lab-reports/4.png)
* transfer files between local and remote computers using the following command, replacing 'zz' with your account-specific letters 

```$ scp <File Name> cs15lsp22zz@ieng6.ucsd.edu:~/```
* you will be prompted to enter your password again; type in your password to complete copying the file to the remote computer
* results should look similar to the screenshot above

## *5. Setting an SSH Key*
![Image](https://dwengxz.github.io/cse15l-lab-reports/5.png)
* you can set an SSH key using the following command
```$ ssh-keygen```
* using this command with prompt you to enter a file to save the key in; store it in the following path
```\Users\<user-name/.ssh/id_rsa```
* you can then write in your new key (it will look like nothing is being typed again), and then use that key to log into your remote account
* the completed process should look similar to the provided screenshot

## *6. Optimize Remote Running*
![Image](https://dwengxz.github.io/cse15l-lab-reports/6.PNG)
* a way you can optimize logging into and running from a remote computer is to set an empty password
* following the steps provided in step 5, set a new SSH key; however, enter nothing to submit a blank password
* this will remove the need to enter your password when entering the remote computer
* the completed process should look similar to the provied screenshot
