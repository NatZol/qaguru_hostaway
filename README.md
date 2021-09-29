# Automation for **Hostaway** site [**https://www.hostaway.com/**](https://www.hostaway.com/)

## Technologies and tools
Tests were written with using Java + JUnit5 + Selenide + Gradle

| Java | Gradle | Junit5 | Selenide |
|:----:|:------:|:------:|:--------:|
| <img src="images/JAVA.svg" width="40" height="40"> | <img src="images/Gradle.svg" width="40" height="40"> | <img src="images/Junit5.svg" width="40" height="40"> | <img src="images/Selenide.svg" width="40" height="40"> |

Tests can be run with Jenkins and Selenoid

| Jenkins | Selenoid | 
|:--------:|:-------------:|
| <img src="images/Jenkins.svg" width="40" height="40"> | <img src="images/Selenoid.svg" width="40" height="40"> | 

The report can be generated with Allure, notification about test run is sent to Telegram

| Allure Report | Telegram |
|:---------:|:--------:|
| <img src="images/Allure Report.svg" width="40" height="40"> | <img src="images/Telegram.svg" width="40" height="40"> |

## For running test job with Jenkins you can use https://jenkins.autotests.cloud/job/07-lady_nata_lie-lesson12/

### Plenty of parameters can be set for test run:

* browser (default browser is chrome)
* browserVersion (default version is 91.0)
* browserSize (default resolution is 1920x1080)
* browserMobileView (mobile device name, for example iPhone X)
* remoteDriverUrl (url address from selenoid or grid)
* videoStorage (url address where you should get video)
* threads (number of threads)
  
You can find below an example of configuration in Jenkins for test run:

### Example of page with set parameters
![alt "Parameters in Jenkins"](./images/jenkinsParamsExample.png)

### How to run tests from command line
Run tests with default parameters:
```bash
gradle clean test
```

Run tests with desirable parameters:
```bash
gradle clean -DremoteDriverUrl=https://user1:1234@selenoid.autotests.cloud/wd/hub/ -DvideoStorage=https://selenoid.autotests.cloud/video/ -Dthreads=2 test
```

### Make a report in Allure:
```bash
allure serve build/allure-results
```
## Tests are run in Selenoid https://selenoid.autotests.cloud/#/
### Test run in Selenoid (example)
![alt "Video from Selenoid"](./images/TestExample.gif "Video from Selenoid")

## Allure report is made after test run with attachments for each test
![alt "Allure report"](./images/AllureNotifications.png)

## Notification with test results is sent to Telegram
![alt "Telegram Notifcation"](./images/TelegramNotifications.png)

## Contact me:
:airplane: Telegram - @lady_nata_lie
