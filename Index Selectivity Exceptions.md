### Index Selectivity Exceptions

Using an indexed field in your query doesn't always make it golden. You can do things in your queries to make them non-selective and thus prone to the dreaded full table scan. When building your queries always strive to avoid these things.

-   Querying for null rows---Queries that look for records in which the field is empty or null. For example:

    ```
    SELECT Id, Name FROM Account WHERE Custom_Field__c = null

    ```


-   Negative filter operators---Using operators such as !=, NOT LIKE, or EXCLUDES in your queries. For example:

    ```
    SELECT CaseNumber FROM Case WHERE Status != 'New'

    ```


-   Leading wildcards---Queries that use a leading wildcard, such as this:

    ```
    SELECT Id, LastName, FirstName FROM Contact WHERE LastName LIKE '%smi%'

    ```


-   Text fields with comparison operators---Using comparison operators, such as >, <, >=, or <=, with text-based fields. For example:

    ```
    SELECT AccountId, Amount FROM Opportunity WHERE Order_Number__c > 10
    ```
