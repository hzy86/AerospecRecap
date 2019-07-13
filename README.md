This is a progress diary for recapping what was a major progress but replaced by something better later.

## Dweetio, Lambda, Cloudwatch, S3 
*7-13-19 Ditched*

Use HTTP GET and params to post data to Dweetio from the LTE shield. Then use Lambda to get data from Dweetio and insert into the database. Schedule Lambda trigger using Cloudwatch.

To deploy, install all packages specified in ```requirements.txt```, and then place them in the same folder as aerospeclambdards.py file that defined a ```handler(event, context)``` function. CTRL+A to select all, right click on aerospeclambdards.py to zip, run ```aws CLI command #1``` in its parent folder to upload to S3, and finally run ```aws CLI command #2``` to update Lambda codes.

Note
- packages and the .py file have to be at the same level in the deployment .zip, otherwise Lambda could not find them
- be sure to modify the Handler in Function codes of of the Lambda setup to match the function name, otherwise Lambda coud not find the main function

Codes - Repo [AerospecUsedCodes/Dweet-Lambda-Cloudwatch-S3](https://github.com/hzy86/AerospecUsedCodes/Dweet-Lambda-Cloudwatch-S3)
- 
- AWSCLIcommands-Lambda.txt

  Two AWS CLI command to script uploading package to S3 and linking it to Lambda.
