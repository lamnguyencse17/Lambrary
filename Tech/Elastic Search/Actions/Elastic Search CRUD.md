# Elastic Search CRUD
## Create
### Create an index
```PUT index_name```
![[Elastic Search Create Index.png]]
### Create a document
- Creating a document can be accomplished with both `PUT` and `POST`
- `POST` will automatically generate an ID
```
POST index_name/_doc
{
	"field": "value"
}
```
![[Elastic Search Create Using POST.png]]
- `PUT` will allow you to create a document with a specific id: Citizen ID, SSN,... aka ID with real meaning
```
POST index_name/_doc/id_you_want
{
	"field": "value"
}
```
![[Elastic Search Create Using PUT.png]]
## Read
### Read a document
```
GET index_name/_doc/id
```