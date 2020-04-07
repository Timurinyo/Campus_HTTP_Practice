Http practice

## Prerequisites:
Have CampusRestHW.exe

## Description:
Create console app with functionality to make http request to following endpoints:

Required headers (all requests):
 - Content-Type : application/json
 - appId : campus-task

[GET]
http://localhost:60214/somedata
http://localhost:60214/somedata?sorted=True
http://localhost:60214/somedata/{id}
cmd: get
flags: --sorted (True/False) ; --id (dataId)
rvalue: error code and message if any, or data specific to request

[POST]
http://localhost:60214/somedata
cmd: post {data}
data required field:
	"dataId": string
	"weight": int

rvalue: status code (always) and message if error

[PUT]
http://localhost:60214/somedata/{id}
cmd: put {id} {data}
data required field:
	"dataId": string
	"weight": int

rvalue: status code (always) and message if error


[DELETE]
http://localhost:60214/somedata/{id}
cmd: delete {id}

rvalue: status code (always) and message if error

## Goal:
Compose a string that tells how many people were killed by the virus in the city.

## Example input: 
>> get   (output)-->    >> []  
>> post {"dataId": "asd", "weight": 13}      -->     >> OK(200)  
>> get    -->      >> [{"dataId": "asd", "weight": 13}]  
>> get --id asd    >> {"dataId": "asd", "weight": 13}  
>> delete asd      >> OK(200)  

