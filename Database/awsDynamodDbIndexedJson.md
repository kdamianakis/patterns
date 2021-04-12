**AWS DynamoDB Indexed JSON**

<u>AWS Pattern</u>

When accessing a DynamoDB table, store the JSON as a STRING as it can support up a large bumber of characters 
(400K at the moment) in the full record including attribute names.

Add elements using the **One AWS Lambda Proxy CRUD Pattern** and within the Lambda for the CRUD populate the 
fields within the DynamoDB record which would then become searchable by the primary index (and sorting key) and 
any additional local or global secondary indexes.

Then utilise a **AWS Search Lambda Pattern** to search via primary and secondary / multiple indeces
until the right information array can be returned back to the LAMBDA function. Since all of the 
DynamoDB information is already part of the JSON file and in sync with the JSON file, only the
JSON files need to be returned back as an array.
