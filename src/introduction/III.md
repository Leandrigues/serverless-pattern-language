# Eventually Consistent as motivation to Data Streaming
Eventually Consistent can make usage of Data Streaming solutions as the core method to replicate data across the multiple databases, specially when dealing with large volumes of data. 

### Use case
Suppose you're building a social network back-end service that stores the user data, such as name and photo. This data can be used from different services, such as by the one that returns the user profile to a web client or by the message chat service. To have this data available to all the services, you could have distributed databases, one per service and replicate the data all over these databases, applying the Eventually Consistent pattern. To do so, a smart way would be to use a streaming service (e.g., AWS DynamoDB streams) that triggers an event whenever a row of the table is updated, and then send it to a function that replicates this data across the other databases.

![img](./III.md)