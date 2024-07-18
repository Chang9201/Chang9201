# Testinfo

Contains information about ground truth for a test instance, including information on time, personnel, and result.

## Endpoints

Testinfo/{testId}

Gets test information for a specific test ID.

## Parameters

### Path Parameters

| Path parameter | Description |
| ------------- | ------------- |
| [testId] | The unique identifier for the test you want to look up. Valid testId values are available from the <sample internal tool> site at sampleurl.com. |

### Query string parameters

| Query string parameter | Required/optional | Description | Type |
| ------------- | ------------- | ------------- | ------------- |
| testevent | Optional | Timestamps for noteworthy events during the test. Default will return test start and end time. | Integer, unix format in MST |
| testpersonnel | Optional |  Information regarding personnel who executed the test. | String |
| testresult | Optional | Result of the test. | String, possible values are "PASS," "FAIL," or "UNKNOWN." |

## Sample request

```
curl -I -X GET "https://api.testinfo.org/data/sampleurl"

```
## Sample response

The following is a sample response from the testinfo/{testId} endpoint:

```
{
    "testinfo": [
      {
          "testId": "12345678",
            "teststart": {
                  "1234567890
        },
            "testend": {
                  "1234567890
        },
            "1234567": {
              "name": "John Doe"
              "role": "Test Engineer"
          },
            "testresult": {
              "PASS"
        }
    }
  ]
}   

```

## Response definitions

The following table describes each item in the response.

| Response item | Description | Data Type |
| ------------- | ------------- | ------------- |
| testId | Unique identifier for the test in the original request. | Integer |
| {teststart} | Start time for test in Unix timestamp. | Integer |
| {testend} | End time for test in Unix timestamp. | Integer |
| {employeeId} | Badge number for the test personnel that executed the test. Employee badge numbers can be found in the internal employee directory. | Integer |
| {employeeId}/name | First and last name of the employee. | String |
| {employeeId}/role | Role of the employee. | Object |
| {testresult} | Result of the test. | Object |
