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
- `PUT` will allow you to create a document with a specific id: Citizen ID, SSN,... aka ID with real meaning. **However this may overwrite the value you want
```
PUT index_name/_doc/id_you_want
{
	"field": "value"
}
```
![[Elastic Search Create Using PUT.png]]
- `PUT` can also be used with `_create` to avoid overwriting an existing document (this will throw an error and do nothing)
```
PUT index_name/_create/id_you_want
{
	"field": "value"
}
```
![[Elastic Search Create Using PUT + _create.png]]
## Read
### Read a document
```
GET index_name/_doc/id
```
![[Elastic Search Read A Document.png]]

## Update
- Update can be done using the same way as [[#Create|create]] by using the existing _id with `POST`.
![[Elastic Search Update with POST _doc.png]]
- The official syntax should be:
```
POST index_name/_update/id
{
	"doc":{
		"field": "value"
	}
}
```
![[Elastic Search Update with POST _update.png]]

## DELETE
```
DELETE index_name/_doc/id_you_want
```
![[Elastic Search Delete a document.png]]