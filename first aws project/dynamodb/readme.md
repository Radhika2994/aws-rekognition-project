I created a table called ImageLabels with:

Partition Key: ImageName

Sort Key: Label

Then, in Lambda, I added code to store each label with its confidence and timestamp.
This taught me how DynamoDB is structured, and why it’s good for fast searches of data.
