# Adobe Experience Manager Tutorial
---
 New Joiner Guide 👨🏾‍💻 
--


May this guide 📖 serve as a handbook to shore up any gaps one may find in their foundations...  


and light the way forward in the journey to becoming an AEM developer. ⚔️

---
---

Dependencies: `Java 11` `Maven` `AEM quickstart jar`

![alt text](https://github.com/matthew-acn/aem_guide/blob/main/dependencies.png)


First, a little house keeping. It is **imperative** to understand and know the following: 
* directory
* file
* IDE
* terminal
* `cd` (command)
* `ls` (command)
* `mkdir` (command)
* `git` (version control software)

A developer **MUST** be able to navigate through their respective machine's directories and files via command line with ease. 

<dl>
  <dt>Windows</dt> 
<dd>If you are unfamiliar with PowerShell, I gift you one command to rule them all: 💍🌋 Get-Command 
 
  Executing this command will output a list of all PowerShell commands available to your machine. </dd>
</dl>  


---
---

Now on to step one...

1. In your terminal, execute ` mkdir` (the name is up to you and you alone are at the helm of this journey).
2. `cd`into the newly created directory.
3. Navigate to https://www.github.com and create a new repository.
4. Back in terminal and within your new directory run `echo "# repo_name_here" >> README.md`
5. Run `git init`
6. Run `git add README.md`
7. Run `git commit -m "your_message_here"
8. Run `git branch -M main`
9. Run `git remote add origin paste_your_git_repo_url` <-- the actual url in case you are confused

Congratulations!! 🥳 You have successfully initialized a git repository! ✨ Yes, yes, you could have just ran git clone "insert url", but that is entirely too lazy! It is better to wield a higher command of your trade than seek the easy way out.


Now, I want you to pay close attention to the following series of commands... as it is actually one giant command that you will **type and execute on one single line**. It is a maven command. It should go without saying that you have by now properly installed java (**version 11**), maven, and AEM quickstart jar. If for any reason you have not, travel here (insert link to AEM setup guide)
