# AEM Authoring Installation Guide


## Establishing a Local AEM development envronment

At the current time of publishing this repository, Adobe does not allow direct access to the Adobe Experience Cloud Downloads website. Hence leading to the need for us to circumvent this dilemma with our solution here.

The following will be stated several times across this markdown file, as the solution is not immediately obvious to the user. When installing AEM, **DO NOT INSTALL THE AUTHORING INSTANCE TO A PATH THAT HAS SPACES IN THE NAMES OF THE DIRECTORY**. This will cause the service to appear as a black screen when hosted on *port 4502*. To be clear this would include the *Program Files* directory within the *C Drive* of **Windows Users** and while the equivalent in **macOS** is *~/Applications* you must still follow the directory naming convention of omitting spaces from directory names.


For clarity in the matter, here is the path containing my AEM quickstart file: **"C:\AEM\quickstart-6.5.jar"**. My solution was to create a directory named *AEM* at the root level of my *C Drive* and as shown here, **"C:\AEM\crx-quickstart\bin"**, I also have *AEM 6.5* itself contained within my AEM directory. As you can see, there are no spaces in my *AEM path*. 

---
Download the AEM Service Package
---

1. Navigate to the *ABG Apprentice Channel*
2. Click **Files** above the chat feed and right of the channel name
3. Locate the file: **aem-service-pkg-6.5.13.0.zip** and click the three dots to the right of the file name
4. Select download
5. After downloading the package, unzip the file and locate it in a **directory path without any spaces in the names**
6. Within the same channel also download the following files: **cq-quickstart-6.5.0.jar** and **license.properties** and store them on the **same level** as the root directory of the **aem-service-pkg**

*Quick note: macOS users automatically unzip compressed files upon downloading so have your intended path ready*

---
Initiate AEM on Localhost Port 4502
---

1. On the *command line* `cd` into the folder containing the **AEM cq-quickstart-6.5.0.jar** file
2. **Windows Users** may simply *double-click* the .jar file  
3. Run the following command: `java -jar -Xmx2g cq-quickstart-6.5.0.jar` <--- if you rename the file it should go without saying that you would type the new name in plafe of the aforementioned
4. Once localhost 4502 appears in your default browser you should see a screen as shown below
5. Enter in the following credentials: User **admin** | PW **admin** and sign in

![alt text](https://github.com/matthew-acn/aem_guide/blob/main/AEM%20admin%20login.jpg)


To continue the tutorial, please navigate to the main [README.md](https://github.com/matthew-acn/aem_guide/edit/main/README.md) file
