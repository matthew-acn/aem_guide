# AEM Authoring Installation Guide
---

## Establishing a Local AEM development envronment

At the current time of publishing this repository, Adobe does not allow direct access to the Adobe Experience Cloud Downloads website. Hence leading to the need for us to circumvent this dilemma with our solution here.
The following will be stated several times across this markdown file, as the solution is not immediately obvious to the user. When installing AEM, **DO NOT INSTALL THE AUTHORING INSTANCE TO A PATH THAT HAS SPACES IN THE NAMES OF THE DIRECTORY**. This will cause the service to appear as a black screen when hosted on *port 4502*. To be clear this would include the *Program Files* directory within the *C Drive* of **Windows Users** and while the equivalent in **macOS** is *~/Applications* you must still follow the directory naming convention of ommitting spaces from directory names.


For clarity in the matter, here is the path containing my AEM quickstart file **"C:\AEM\quickstart-6.5.jar"**. My solution was to create a directory named *AEM* at the root level of my *C Drive* and as shown here, **"C:\AEM\crx-quickstart\bin"**, I also have *AEM 6.5* itself contained within my AEM directory. As you can see, there are no spaces in my AEM path. 
