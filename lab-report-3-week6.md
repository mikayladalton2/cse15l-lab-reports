## Lab Report 3

# Streamlining `ssh` Configuration

1. **`ssh` Config File**
---
Firstly, change the directory to .ssh, and then use the `cat >` command to create a new file and add content to it. Then, do `cat config` to confirm the content got added. 
![Adding text to Config File](Add%20text%20to%20config%20file.png)

2. **`ssh` Command**
---
We are now am able to run the command `ssh ieng6` and log into our acccount. So much easier!
![`ssh` Command](ssh%20command.png)

3. **`scp` Command**
---
Another super convenient feature of this is we can copy over a file from our computer to our remote account in one simple line of code: `scp text.txt ieng6:~/` without even having to fully log in. How nice is that!!
![Copying over file](copying%20over%20file.png)

# Setup Github Access from ieng6

1. **Keys on Remote Account**
---
The last line of code in this screenshot shows where the public key and private keys are stored on my remote account.
![Keys in Remote Account](setting%20up%20keys%20remote.png)


2. **Keys on Github**
---
This screenshot shows where the public key is located on my github. Follow this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) for steps on adding keys to github. 
![Github public key location](github%20public%20key.png)

You must run the two following commands to in order to add the private key.
![private key added](private%20key%20.png)

3. **Commit and Push Changes**
---
At this point, you should be able to commit and push any changes to github. I am not sure why mine isn't working as the public key is stored on both my remote account and github.
![commit and push changes](commit%20and%20push%20changes.png)
 

# Copy whole directories with `scp -r`

1. **Copying over markdown-parse directory**
---
Using the command `scp -r *.java *.md lib/ ieng6:markdown-parser`, we can copy over the markdown-parser directory to our remote account. I specifically copied over the java and md files as well as the lib folder. 
![Copying over directory](copying%20over%20directory.png)

2. **Logging into Remote Account and Running Tests**
---
Now, we can log into our ieng6 account and switch to markdown-parser directory and compile and run tests in MarkdownTest.java!!!
![Running tests on Remote Account](running%20tests%20on%20remote.png)

3. **Combining Commands**
---
We can condense all this to one command line arugment through the use of `scp`,`;`, and `ssh`. It is important to note that because this is on the remote account, it does not have access to the java we have downloaded on our computers. So, I had to include the following two lines before compiling and running respectively, `/software/CSE/oracle-java-17/jdk-17.0.1/bin/javac`,  `/software/CSE/oracle-java-17/jdk-17.0.1/bin/java`.
![Combining Commands](Combining%20commands.png)