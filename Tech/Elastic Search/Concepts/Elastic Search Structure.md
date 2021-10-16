# Elastic Search Structure
## Node
![[Elastic Node.png]]
- Node is an instance of elastic search
- Have a unique id and a name
- Belongs to a [[Elastic Search Structure#Cluster|cluster]]
- A single node can be a cluster

## Cluster
![[Elastic Cluster.png]]
- Cluster can have many nodes
- Nodes in a cluster will accomplilsh a common task
- Nodes are assigned to one or many roles. One of which is storing [[Elastic Search Documents Storing|data]]
