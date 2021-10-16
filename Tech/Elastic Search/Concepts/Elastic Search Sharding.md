# Elastic Search Sharding
- Shard is where [[Elastic Search Documents Storing|data]] is stored
- A shard is created by default when an [[Elastic Search Index|index]] is created
- ES can be configured to have multiple shards distributed over multiple [[Elastic Search Structure#Node|nodes]] and it is called **sharding

# Types of Shard
![[Elastic Search Shard Types.png]]
## Primary Shard
Primary shard is the original shard where the data is store
## Replica Shard
- Replica Shard is a copy of [[#Primary Shard|primary shard]] and stored in a different [[Elastic Search Structure#Node]]
- If a [[#Primary Shard|primary shard]] goes down and data is lost, a replica shard corresponding to the [[#Primary Shard|primary shard]]can provide a backup
- Replica shard can also improve the search performance of a [[#Primary Shard|primary shard]]. E.g:


