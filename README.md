# 7PNordicAS_Test_Selenium2

General:
For the task below you could choose ANY webpage that is having HOME page and LOG IN option.
Except the technology stack task does not have the best way to solve it. We appreciate your approach to the solution and consider it as a good topic to discuss on technical interview.
In case of any questions please contact.
Task:
1. Create test plan which describes how to text tests next functionality / features:
a. Home page is having correct title
b. Web page login – positive scenario
c. Web page login - negative scenario
2. Automate test cases a, b and c for any browser using the next technology stack
a. Selenium
// b. webdriver.io (https://webdriver.io/)
// c. Cucumber framework (Gherkin Syntax).
// NB. As a sample you could use e.g https://github.com/webdriverio/cucumber- boilerplate
3. Add the needed instructions how to install and execute automated test cases in order to check the task.
4. Send the ready project to the email or the link to the git repository (repository is preferred).

I have choosen the web page https://hack.me/

To resolve the task I were using the following technologies: chromeDriver, Selenium, TetsNG suit, annotations, Maven, java. 
To use the offering technologies under letters b. and c. are also appropriate, but as they are new for me it will take more time to learn and implement
them appropriately. After reviewing them I loved them and in any case, I will create some test cases also.

Shortly my test plan.

1. To test the correctness of the Home page title is need to implement one test case where the actiual result is known. 

2. Positive scenario:

Data: login: X password: Y

User Log in correctly using proprietary data
3. Negative:

3.1. Data:

login: [not registered login] V password: Y

User can't log in with unregistered login

3.2. Data:

login: X password: [Bad password] B

User can't log in with proprietary login and bad password
Pre condition: System unavailable

3.3. Data:

login: X password: Y

User can't log in to system with proprietary login and password (servers are down, no internet connection, etc )

     
Instruction how to install and execute:

What needs to install and adjust:
1. JDK file https://www.oracle.com/java/technologies/javase-downloads.html 
2. chromedriver https://chromedriver.chromium.org/downloads and add the path to the file. For Mac: https://www.kenst.com/2015/03/including-the-chromedriver-location-in-macos-system-path/ For Windows: https://developers.refinitiv.com/sites/default/files/How%20To%20Add%20ChromeDriver%20To%20System%20Variables_0.pdf 

3. Add to the java files where needed the path where the cromedriver file is located: System.setProperty("webdriver.chrome.driver", "//User/Downloads/chromedriver");

4. you can also create jar file:
cd-  javac TestSuites.java

java TestSuites.java

5. Then if needed (it is not necessary) for Windows create run.bat file where add the path to the jar file:
java -jar .\TestSuites.jar

I have been executed TestNG.xml suite directly from Intellij Idea debug tools. 
