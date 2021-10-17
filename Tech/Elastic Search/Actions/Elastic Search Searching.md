# Elastic Search Searching
## Get all documents from an index
```
GET index_name/_search
```
- A sample of 10 search results will be displayed by default
- However the total hits `relation` can be `lte`, `eq`, `gte`. If you want to know the exact number of hits add this option:
```
GET index_name/_search
{
	"track_total_hits": true
}
```
![[Elastic Search GET all documents.png]]

## Get some specific documents
- You can get some specific documents by using `query` field
- By default it will use `OR` logic for `match` query
```
GET index_name/_search
{
	"query": {
		"query_type": {
			"field_name": "value or value_object"
		}
	}
}
```
![[Elastic Search GET with query.png]]

## Aggregations
- Aggreations is used to summarizes data as metrics, statistics, and other analytics
```
GET index_name/_search
{
	"aggs": {
		"aggregation_name": {
			"aggregation_type": {
				"field": "field_name",
				"size": "size_of_field"
			}
		}
	}
}
```
![[Elastic Search Aggregations.png]]

- `Aggregations` can be used with `Query` to perform analytics on specific documents
![[Elastic Search Query + Aggregations.png]]