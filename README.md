# LoadTestJmeter
**Precondition:**
1. Jmeter installed


**Steps to run sample load test server with senario get issue detail and get list attachment of issue**
1. Open file src/TestPlanJiraServer.jmx and edit: 
- *jmeterpath*: current source locator
- *jiraUrl*: site in test
- *getIssuePath*: path get issue detail api
- *getAttachmentPath*: path get issue attachment api
- *protocal*: emum(https, http)
- *ThreadGroup.num_threads*: number of thread run test
2. Update the user test set in file *data/jira_9_user.csv*
3. Run test with comment: *<JMETER_HOME>/libexec/bin/jmeter.sh -n -t src/TestPlanJiraServer.jmx -l report/result.csv -e -o report/Dashboard*
4. Check the html report in the *report/Dashboard*


**Steps to run sample load test UI with senario login and view issue detail screen**
1. Open file *src/TestPlanCheckUI.jmx* and edit variable: 
- *jmeterpath*: current source locator
- *jiraUrl*: site in test
- *getIssuePath*: issue in test
- *ThreadGroup.num_threads*: number of thread run test
2. Update the user test set in file *data/jira_cloud_user.csv*
3. Download chromedirver compatible with current OS and paste in to folder *chromedriver*
3. Run test with comment: *<JMETER_HOME>/libexec/bin/jmeter.sh -n -t src/TestPlanCheckUI.jmx -l report/resultUI.csv -e -o report/DashboardUI*
4. Check the html report in the *report/DashboardUI*

**Note:** JMETER_HOME with homebrew installer: */opt/homebrew/Cellar/jmeter/5.5*
