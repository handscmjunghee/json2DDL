# json2DDL
Convert json data into DDL

A simple json to DDL tool, very useful when doing ETL.

<br/>

Currently supported json and database type relationships:

|json|DDL|
|--|--|
|number|bigint|
|string|varchar|
|boolean|tinyint|
|Date|datetime|
|`Array` \|| `object`|json|
|`null` \|| `undefined`|null|
|other|undefined|

<br/>

It currently has some built-in basic rules:

1. If an attribute is of json type, the corresponding database type is longtext
2. Other types will be converted to String first, and then *2 is the length of the database type
3. The decimal type in json (such as: `1.23`) corresponds to the `varchar` type in DDL
