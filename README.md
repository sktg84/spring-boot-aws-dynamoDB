# Spring Boot AWS DynamoDB

DynamoDB is a Document style database. In other words semi-structured database. It has the capability 
to scale depending upon the size of data, And it supports 35 levels of nesting on data. Data is stored 
in solid state drives, and is spread across 2 geographical datacenter so data can never be lost.

DynamoDB supports two types of primary key attributes

    single attribute - Hash Key/Partition Key
    this hash key is used to calculate the hash value which is then used to determine the physical 
    location where the data will be stored
    no two keys can have same values in single attribute 
    
    composite attribute - Hash Key + Range Key/Sort Key
    this is a combination of hash key and a range key.
    two items can have same hash key but different range key

You can use DynamoDB directly from the cloud environment or you can use the dynamodb local a downloadable version provided by amazon

In this example, we are going to directly connect and work with the cloud version

DynamoDBMapper is a Object mapper for domain-object interaction with DynamoDB.

DynamoDBSaveExpression - you can use this to adding multiple expressions for your need. 
For example, you may want to save only if an attribute has a particular value.

ExpectedValue - it represent a condition to be compared with an attribute value


JSON to use:
post -> http://localhost:9001/dynamoDb
{
 
 "lastName":"PK",
 "firstName":"Rithhvi",
 "age":"10",
 "address":{
	"addressline1":"5 kannammal st",
	"addressline2":"hasthinapuram",
	"state":"tn",
	"city":"chennai",
	"zipCode":"12345"
	}
}

get -> http://localhost:9001/dynamoDb?studentId=c415acc1-7db7-4ee8-bec2-fc2c474e7bfb&lastName=PK
