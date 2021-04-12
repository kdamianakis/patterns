**One AWS Lambda Proxy CRUD Pattern**

<u>AWS pattern</u>

When using a serverless - API gateway pattern, create one Lambda to deal with 
CRUD - Create, Read, Update and Delete matching into the standard REST API POST, 
GET, PUT and DELETE methods.

Deal with the methods within the function. If needed, utilise LAMBDA 
CHAINING patterns to follow it through, though ideally the whole process
can be completed in a single Lambda.

This lambda would work well with the **AWS DynamoDB Indexed JSON** pattern.
