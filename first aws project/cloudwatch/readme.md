Testing and CloudWatch Logs:
To make sure everything worked, I:

Checked S3 → saw .labels.json generated

Checked DynamoDB → saw labels stored correctly

Checked CloudWatch logs → saw Lambda executed successfully

Checked SNS → received email alert

From this, I understood the importance of logs and monitoring, especially in serverless apps where you don’t have a traditional server console.

