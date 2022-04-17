# Lab Report 1


### **Installing VS Code**
![VS Code](VS%20Code.png)

Installing VS Code is very easy. Simply open this
[link](https://code.visualstudio.com/) and click download, select the type of computer you have, and voila! It really is *that* easy. 


----
## **Remotely Connecting**
![Remotely Connecting](Remotely%20Connecting.png)
So the first step to remotely connecting is to open up your VS Code terminal. From there, run the command `ssh cs15lsp22zz@ieng6.ucsd.edu` with the zz replaced by the letters in your course specific account. For example, mine is aqa. 

Then, a message should come up that prompts you to type in your password. If all was done correctly, a message similiar to the one in the image above should pop up. This means you have successfully remotely connected, woohoo!


----
### **Trying Some Commands**
![Trying Some Commands](Trying%20Some%20Commands.png)
Try running some commands in VS Code terminal such as `ls`, `cd`, `pwd`, `mkdir`, and `cp` to get comfortable with the commands and what exactly they do. Once you get comfortable, you can try running more specific commands such as the ones in the image above. 


---
### **Moving Files with scp**
![Moving Files with scp](Moving%20Files%20with%20scp.png)
The `scp` commands allows you to copy a file from your computer to a remote computer. This command is ran from the client(your computer, AKA not logged into ieng6). Run the `scp` command followed by the name of the file you want to copy over. You will be prompted to enter your password. If all goes well, you should be able to see your file in the home directory(you can check this by using the command `ls`). 

---
### *Setting an SSH Key*
![Setting an SSH Key](Setting%20an%20SSH%20Key.png)
SSH keys take care of the hassle of continuously having to retype in your password when switching between the client and server. The idea is you copy the public key onto the server and the private key onto the client. The `ssh` command can use the pair of files in place of your password. Steps to do this:

1. (on client) run command `ssh-keygen`
2. hit enter when prompted for a passphrase
3. hit enter again when prompted to enter passphrase again
4. run command `ssh cs15lsp22zz@ieng6.ucsd.edu` and enter password
5. `mkdir .ssh` (make directory)
6. logout of server
7. last step!! run command `scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys` and type in your password.

---
### **Optimizing Remote Running**
![● Optimizing Remote Running](Optimizing%20Remote%20Running.png)
For optimizing Remote Running, you can practice writing multiple commands on one line and using the up arrow key to save time. You can edit the file, upload it to the remote server and run it. 