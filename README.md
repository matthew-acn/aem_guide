# Adobe Experience Manager Tutorial
---
 New Joiner Guide 👨🏾‍💻 
--


May this guide 📖 serve as a handbook to shore up any gaps one may find in their foundations...  


and light the way forward in the journey to becoming an AEM developer. ⚔️

---
---

Dependencies: `Java 11` `Maven` `AEM quickstart jar` `AEM service package` `Typescript` `npm` `node` 

![alt text](https://github.com/matthew-acn/aem_guide/blob/main/dependencies.png)

If you have yet to install the required dependencies, please refer to the guide linked [here](https://github.com/dylansql/aem-guide-dependency-installation) <-- here will redirect to a setup guide in the repo

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
Create the Directory
--

1. In your terminal, execute ` mkdir` "directory_name" (the name is up to you and you alone are at the helm of this journey).
2. `cd`into the newly created directory.
3. Navigate to https://www.github.com and create a new repository.
4. Back in terminal and within your new directory run `echo "# repo_name_here" >> README.md`
5. Run `git init`
6. Run `git add README.md`
7. Run `git commit -m "your_message_here"`
8. Run `git branch -M main`
9. Run `git remote add origin paste_your_git_repo_url` <-- the actual url in case you are confused

Congratulations!! 🥳 You have successfully initialized a git repository! ✨ Yes, yes, you could have just ran `git clone "insert url"`, and that is entirely dealer's choice! However, it is better to wield a higher command of your trade than to seek the easy way out.


---
---
Generate the Maven Archetype
--
Now, I want you to pay close attention to the following series of commands... as it is actually one giant command that you will **type and execute on one single line**. It is a maven command. It should go without saying that you have by now properly installed Java (**version 11**), Maven, and the AEM quickstart jar. If for any reason you have not, travel here (insert link to AEM setup guide)

Within the same root directory that initialized the git repository, execute the following:

```
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate 

-D archetypeGroupId=com.adobe.aem 

-D archetypeArtifactId=aem-project-archetype

-D archetypeVersion=35 

-D appTitle="whatever you want to name it" 

-D appId="shortened version of the title name"

-D groupId="com.adobe.aem.anything.you.want" 

-D artifactId="aem-anything"

-D package="com.adobe.aem.anything" 

-D version="0.0.1-SNAPSHOT"

-D aemVersion="cloud"
```


Here is a screenshot from my terminal if you find yourself unsure of how that would look:

![alt text](https://github.com/matthew-acn/aem_guide/blob/main/mvn%20com.png)


Once you have executed the command, run `ls` and `cd` into the aem directory created by the Maven archetype.

If you run `ls` again you should see a file structure similar to my Maven archetype as shown below:

![alt text](https://github.com/matthew-acn/aem_guide/blob/main/Maven%20archetype.png)


---
---
Updating Typescript
---

If you were to attempt to build your project as is... it would currently fail the build. This is due to a mismatch in the *archetype* and *typescript* version. To remedy this, you will need to follow a few simple steps.

1. In your command line and within the project directory, run `npm install typescript@latest -g`
2. Next locate the **package.json** file in the **ui.frontend** directory 
3.Scroll down to the listed *typescript dependency version*
4. Update the **package.json** file with the **latest version of typescript**

Here's a screenshot of my file as it appears in the IntelliJ IDE
![alt text](https://github.com/matthew-acn/aem_guide/blob/main/Typescript%20version.jpg)

---
---
Create a Project Build 
---

If you haven't already downloaded and installed **AEM 6.5** please click [here](https://github.com/matthew-acn/aem_guide/blob/main/AEM.md)

1. Ensure you have a local instance of AEM running
2. `cd` into the directory where you generated the archetype
3. Run the following command: `mvn clean install -PautoInstallSinglePackage`

**If you have followed the tutorial to the letter, the terminal will out put "Build Success" and are ready to proceed**
**If you are met with "Build Failure" of any kind, step back thorough the tutorial to find your mistake. And if that should still fail you, take to your search engine of preference and deploy your research skills**

