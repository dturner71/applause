#Installing Appium:
> http://appium.io/

**Installing From the command line:**

* Install brew

ruby -e “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

* get node.js

brew install node     
 
* get appium

npm install -g appium  

* get appium client

npm install wd     
  
* start appium

appium &    
           
#Clone the git repo 
git clone https://github.com/getPlutus/test-automation.git

* import it as a maven project in eclipse.

#Install eclipse testNG plugin:

> http://testng.org/doc/download.html

#Configureing the test

* Select the test .xml file you wish to run stored in src/test/java:

Edit the following in the xml file:

name="fullReset" value="true" 
> True: if the app is installed, uninstall it and install app. 

> False: if the app is already installed test that.

name="app" value="/<pathToApp>/wallet-debug.apk" 
> Location of the apk or ipk file

name="platformName" value="Android" 
> android or iOS

name="platformVersion" value="4.4" 
> Version of the os

name="deviceName" value="26e7b8e4"> 
> UID of device

	
**Example command lines 

mvn clean test -DsuiteXmlFile=src/test/java/signInTest_Simulator.xml -Dapp=/Users/davidt/appStorage/Simulator/*app_name* -DdeviceName='iPad Retina'

mvn clean test -DsuiteXmlFile=src/test/java/signInTest_device.xml  -Dudid=de6a12264f2caeab8526fc586f56e53b012b30a9

