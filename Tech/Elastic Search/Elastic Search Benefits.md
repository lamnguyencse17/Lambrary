# Elastic Search Benefits
- Much faster searching than most database with better query support
- Provides fast and relevant search results
- Powerful and distributed by using [[Elastic Search Sharding|sharding]] and scaling the number of [[Elastic Search Structure#Node|nodes]]. E.g:
	- One node needs to perform a query on 500k documents take 10 seconds
	- Ten nodes holding 50k perform the same query can take 1 second
- Reliable with using [[Elastic Search Sharding#Replica Shard|replica shard]] to backup [[Elastic Search Documents Storing|data]]