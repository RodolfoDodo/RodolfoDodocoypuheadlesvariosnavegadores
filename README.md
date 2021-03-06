﻿# SpecFlow-coypu-custom-webdriver template
#### with SpecFlow, Coypu, custom IWebDriver for Coypu SessionConfiguration and Coypu BrowserSession manager to run browsers:
* ##### chrome (default browser)
* ##### firefox
* ##### internet explorer
* ##### chrome headless
* ##### firefox headless

### Prerequisites 1
* chromedriver.exe (put it into project root)
* geckodriver.exe (put it into project root)
* IEDriverServer.exe (put it into project root)

### Prerequisites 2 (managed by VS Extensions and Updates)
* SpecFlow for Visual Studio (2017)
* Markdown Editor
* Dotnet Extensions for Test Explorer

### Prerequisites 3 (managed by VS NuGet Package Manager)
* SpecFlow
* SpecFlow.NUnit
* NUnit
* NUnit.Console
* NUnit3TestAdapter
* NUnitV2.Core
* ReportUnit
* SpecFlow.NUnit.Runners
* TestReport.SpecFlow
* Selenium.WebDriver
* Coypu

### Initial
* clone repository
* open 'Manage nuGetPackage for solution' and install packages
* in 'Properties' for chromedriver.exe, geckodriver.exe and IEDriverServer.exe change 'Copy to Output Directory' to 'Copy always'

### Customise SpecFlow tests
* add your .feature files with scenarios
* create custom steps class / steps classes
* generate steps- in .feature file open context menu and choose 'Generate Step Definitions'
* create custom page objects classes and assertions classes with methods
* delete example .feature files, steps classes, page objects classes and assertions classes
* to customise location of 'TestReportSpecFlow' directory, go to App.config, find appSettings with key 'testResultFolder' and change its value

### How to run tests:
#### With command (Package Manager Console):

##### To run SpecFlow tests with NUnit.ConsoleRunner and with default browser, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

##### To run SpecFlow tests with NUnit.ConsoleRunner and with chrome, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --params:BROWSER=CHROME --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

##### To run SpecFlow tests with NUnit.ConsoleRunner and with firefox, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --params:BROWSER=FIREFOX --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

##### To run SpecFlow tests with NUnit.ConsoleRunner and with internet explorer, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --params:BROWSER=INTERNETEXPLORER --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

##### To run SpecFlow tests with NUnit.ConsoleRunner and with chrome headless, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --params:BROWSER=CHROMEHEADLESS --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

##### To run SpecFlow tests with NUnit.ConsoleRunner and with firefox headless, type:
* nunit3-console specflow-coypu-custom-webdriver\bin\Debug\specflow-coypu-custom-webdriver.dll --params:BROWSER=FIREFOXHEADLESS --work=NUnitTestResult --out=NUnitTestResult.txt --result=NUnitTestResult.xml

#### With IDE (Test Explorer):
* run tests with Test Explorer
* or run .feature file / directory with .feature files / scenario in .feature file

#### Reports and screenshots
##### Generate report from command (ReportUnit):
* reportunit "NUnitTestResult" "NUnitReports"

##### For tests running from command: 
Reports are placed in 'NUnitReports' directory, after generating them with commandline
To run generated report in browser, open 'Index.html' file.

##### For tests running from IDE: 
Reports are also placed in 'TestReportSpecFlow' directory, , including screenshots of failed scenarios
To run generated report in browser, open 'TestReport.html' file.


