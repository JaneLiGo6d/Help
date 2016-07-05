# Broadleaf Development Setup Guide
The Broadleaf installation has the following steps:
1. Install Java 8.0
2. Install Maven
3. Download Broadleaf
4. Install Spring Tool Suite(STS)

## 1. Install Java 8.0
1.	Download the Java file.
`jdk-8uversion-macosx-x64.dmg` from Oracle Java website.
Before the file can be downloaded, you must accept the license agreement.
2.	From either the Downloads window of the browser, or from the file browser, double click the .dmg file to launch it.
A Finder window appears containing an icon of an open box and the name of the .pkg file.
3.	Double click the package icon to launch the Install app.
The Install app displays the Introduction window.
4.	Click Continue.
The Installation Type window appears.
5.	Click Install.
A window appears that says "Installer is trying to install new software. Type your password to allow this."
6.	Enter the Administrator login and password and click Install Software.
The software is installed and a confirmation window appears.
7.	After the software is installed, delete the .dmg file if you want to save disk space.
8.	Configure the path, In terminal :
```bash
$ cd ~
$ touch .bash_profile
$ vi .bash_profile
```
Add the following conents to the .bash_profile:
> export JAVA_HOME='/Library/Java/JavaVirtualMachines/jdk1.8.0_92.jdk/Contents/Home'
> export CLASSPATH=.:$JAVA_HOME/lib:$JAVA_HOME
> export PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin

Test your Java installation:
```bash
$ source .bash_profile
$ java –version
```
You should see something like the following:
> java version "1.8.0_92"
> Java(TM) SE Runtime Environment (build 1.8.0_92-b14)
> Java HotSpot(TM) 64-Bit Server VM (build 25.92-b14, mixed mode)

## 2. Install Maven
1.	download the maven file
`apache-maven-3.3.9-bin.tar.gz` from Apache Maven site  https://maven.apache.org/download.cgi
2.	extract `apache-maven-3.3.9-bin.tar.gz` to directories ,for example : ``/Users/MyUsername/apache-maven-3.3.9`
3.	open terminal ,set maven path in `~/.bash_profile`
> export M2_HOME=/Users/MyUsername/apache-maven-3.3.9
> export PATH=$PATH:$M2_HOME/bin

Verify the installation:
```bash
$ source ~/.bash_profile
$ mvn –v
```

## 3. Download Broadleaf
Broadleaf changed its license after version 5.0. Therefore we use version 4.0.5-GA.
1. Download Broadleaf core source code and unzip it to your project folder. https://github.com/BroadleafCommerce/BroadleafCommerce/releases/tag/broadleaf-4.0.5-GA
2. Download Broadleaf demo site source code and unzip it to your project folder. https://github.com/BroadleafCommerce/DemoSite/releases/tag/broadleaf-4.0.5-GA

## 4. Install and Configure Spring Tool Suite (STS)
After download and install Spring Tool Suite from https://spring.io/tools,
configure/customize STS:
1.	create a new directory and start STS using the newly created directory as
its workspace directory.
2. Unzip the two Broadleaf project files into the workspace directory.
3. import DemoSite-broadleaf-4.0.5-GA

![p1](images/Picture1.png)

![p2](images/Picture2.png)

click next and in the box for "Root Directory" enter the path to the
directory that you saved your DemoSite-broadleaf-4.0.5-GA to on
your filesystem, or hit the "Browse..." button next to the input box to
browse for the location. After you do that, you should now see 4 different
projects pop up:

![p3](images/Picture3.png)

Note that there is a checkbox for "Add project(s) to working set" and the value is defaulted to `ecommerce-website`. Working sets will become important later, but we can leave this like it is for now.
