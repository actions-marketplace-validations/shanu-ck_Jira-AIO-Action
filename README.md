# Jira AIO Action

[![Test AIO Jira Action](https://github.com/ShanuDey/Jira-AIO-Action/actions/workflows/TestJiraAioAction.yml/badge.svg)](https://github.com/ShanuDey/Jira-AIO-Action/actions/workflows/TestJiraAioAction.yml)

## Usage
    - name: Jira AIO Tests with Github Action
      uses: ShanuDey/Jira-AIO-Action@v2
      with:
        token: ${{ secrets.AIO_API_TOKEN }}
        filePath: "testReport/JsonReport.json"
        jiraProjectKey: "FIR"
        aioCycleKey: "FIR-CY-1"

| Input| Description | Required | Default |
|--|--|--|--|
| token | AIO API Token is required to interact with AIO Tests | Yes | |
| createNewRun | Creates a new run for each case | No | true |
| addCaseToCycle | If case is not already existing in the cycle, then the case is added to the cycle.  False will mark such  a case in failures | No | true |
| createCase | f a key or automation key is not found in the tags, then a new case will be created if set to true. | No | true |
| bddForceUpdateCase | If the automation results file has different steps then the mapped case in AIO Tests, then they would be overwritten with the one from the results file if the value is set to true | No | true |
| filePath | File path of the test report | Yes | |
| fileType | File type of the test report | No | json |
| jiraProjectKey | Mention the Jira Project Key | Yes | |
| aioCycleKey | AIO test cycle key | Yes | |
| reportType | Test result type E.g. Cucumber | No | Cucumber |

## Developed By
* [ShanuDey](https://github.com/ShanuDey)
* [paypal.me/ShanuDey](Paypal.me/ShanuDey)

