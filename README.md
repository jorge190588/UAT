## Automated web tests for Angular App using Selenium, Serenity, Gherkin, Cucumber and Maven

A simple example of some BDD-style automated acceptance criteria, running against AngularJS Forms.

Run the tests like this:

```
mvn clean verify
```

By default, the tests run with chrome, so you will need this installed. Otherwise, if you prefer Firefox ( version <= 46), modify the serenity.properties file or run the tests like this:
```
mvn clean verify -Dwebdriver.driver=chrome
```

The reports will be generated in `target/site/serenity`.


BDD: Java Maven Cucumber Selenium Setup
==================================

Java + Serenity + Cucumber + Gherkin + Selenium BDD test cases

This repo contains the Maven setup for Cucumber / Selenium, with filling the form as example code, which can be run on local or connect to remote SaucsLabs / TestingBot for cross browser testings. It helps to setup a BDD environment for User Acceptance tests.

This repo can be run on local Windows / Mac / Linux Platform, as long as you have Java/Maven setup correctly.


Setup
=

Install on Local Machine 
=

Install Java & Maven on your local machine

To Run (Standalone) 
=
```
Run as Junit test on Runner class(Right click on the class which is annotated by @RunWith(CucumberWithSerenity.class))
```

To Run (Maven command line) 
=
```
Local machine with browser name (ie / chrome / firefox / safari)

- Test with Google Chrome (Mac / Windows for machineType):
> mvn test -DsiteUrl=http://www.google.com -DbrowserName="googlechrome" -DmachineType="mac"

- Test with Firefox (Mac / Windows for machineType):
> mvn test -DsiteUrl=http://www.google.com -DbrowserName="firefox" -DmachineType="mac"

- Test with IE (Windows Only):
> mvn test -DsiteUrl=http://www.google.com -DbrowserName="ie"

- Test with Safari (After install Safari extension, see /drivers/README.md):
> mvn test -DsiteUrl=http://www.google.com -DbrowserName="safari"
```
Remote Webdriver:
```
- BrowserStack (You can pass through Bamboo/Jenkins build variable for api key)
> mvn test -DsiteUrl=http://www.google.com -DenvName="remote" -DremoteWebDriver="http://<browserstack api key>@hub-cloud.browserstack.com/wd/hub" 

- SauceLabs (You can pass through Bamboo/Jenkins build variable for api key)
> mvn test -DsiteUrl=http://www.google.com -DenvName="remote" -DremoteWebDriver="http://<saucelabs api key>@ondemand.saucelabs.com:80/wd/hub"

- Testingbot (You can pass through Bamboo/Jenkins build variable for api key)
> mvn test -DsiteUrl=http://www.google.com -DenvName="remote" -DremoteWebDriver="http://<testingbot api key>@hub.testingbot.com:4444/wd/hub"

```

WebDriver Update
=
See README inside /drivers folder and update the relative path in serenity properties.

Before we start
=

Feature file: Gherkin Syntax 
=
Gherkin is the language that Cucumber understands. You can find more Gherin Syntax here:
```
https://github.com/cucumber/cucumber/wiki/Gherkin
```

Selenium Syntax 
=
Selenium is an automated web browser testing. You can find some commonly used Selenium commands here:
```
http://www.seleniumhq.org/docs/02_selenium_ide.jsp#commonly-used-selenium-commands
```

# Configure Project

## Open intellij

Open intellij and make click in update imports.

## Configure SDK AND JDK.

1. Open project Structure
2. Select SDKs option in Platform Sttings section
3. Click on add (+) button
4. Select JDK option
5. Find the root where jdk is located, Example: C:\Program Files\Java\jdk1.8.0_161
6. Click on OK button







