# CUC-JMeter
Performance and Load tests
Installation
Java
JMeter requires Java to run, so you'll have to install it if you don't have it already. To check whether you have Java installed, open up a terminal and type "java -version". 
If you already have Java installed you can skip to the next step.  Otherwise:
QUICK:
Download and installed the OpenJDK as identified from the IP documentation
Once you've downloaded and installed Java, check that everything is installed using the command "java -version".
DETAILED: see the following page
System Setup (Windows)
Look for the Java section with the NOTES.
System Setup (Mac)
JMeter
Download and install JMeter from  (see instructions below for more help).
On Windows
Choose (or create) a download file on your hard drive (C:\).
On the JMeter site (here), in the "BINARIES" section, download the .zip version to the folder (directory) you created.
(Unless you want to build from Source, and you may not need these instructions.)
Once the file is downloaded, rght-click on the .zip > Extract All
Don't accept the default location unless you enjoy multiple nested folders with the same name.
Instead, browse to folder where you want to install it, and extract to that folder.
When it unzips, the files and folders will be in a new folder with the name of the current jmeter version.
To start:
Option 1:
Open the folder with the jmeter version name.
Open the bin folder.
Double-click on jmeter.bat
Option 2:
Open a command prompt.
Navigate to the folders specified above.
Type jmeter.bat at the prompt, and type the ENTER key.
JMeter should start.
Reference: https://guides.flood.io/scripting-and-tools/jmeter/download-and-install-jmeter

Creating an example Test Plan
Create a simple Test Plan to send a singular GET request to the ChurchofJesusChrist.org homepage.  Note as JMeter is a protocol-level utility, only the initial page will be requested and not all of the additional resources (e.g. images, javascript, css, etc.) used to properly render the page.  The JMeter Recorder can be used to more quickly create complex Test Plans that simulate an actual browser request.

Start JMeter
To open JMeter, go to the directory where it was installed and run either jmeter.bat (for Windows users) or the jmeter executable (for Linux users) in the /bin directory.
Create a Thread Group
Right click on Test Plan > Add > Threads (Users) > Thread Group
Add an HTTP Request Sampler
Right click on Thread Group > Add > Sampler > HTTP Request
Configure the HTTP Request
Click on the newly created HTTP Request
Name: www.churchofjesuschrist.org/?lang=eng
Protocol: https
Server Name: www.churchofjesuschrist.org
Path: /
Add a new Query Parameter by clicking the Add button at the bottom of the HTTP Request
Name: lang
Value: eng


Running a Test Plan
To view the results of a test run, Listeners are used to capture the resulting data.

Add a Listener to your Test Plan
Right click on Thread Group > Add > Listener > View Results Tree
Save your test plan.
Under the jmeter folder, maybe make a folder like, "test_plan".
Rename the .jmx file.
Save.
Run the test in JMeter by clicking the Play button
Verify the test status under the View Results Tree Listener


Congratulations! You've now created and run your first Test Plan in JMeter!
