# Testinfo

Contains information about ground truth for a test instance, including information on time, personnel, and result.

## Endpoints

Testinfo/{testId}

Gets test information for a specific test ID.

## Parameters

### Path Parameters

{testID} - The specific test ID for the test you want to look up. Values are available from appleinternaltoolexample.com.

### Query string parameters


| Query string parameter | Required/optional | Description | Type |
| ------------- | ------------- | ------------- | ------------- |
| teststart | Optional | Time when the test was started. | Integer, unix format in MST |
| testend | Optional | Time when the test finished running. | Integer, unix format in MST |
| testpersonnel | Optional | Names (first and last name) of personnel who executed the test. | String |
| testresult | Optional | Result of the test. | String, possible values are "PASS," "FAIL," or "UNKNOWN." |


teststarttime - The start time Integer. Unix format in MST
testendtime - Integer. Unix format in MST
testpersonnel - 
testresult



