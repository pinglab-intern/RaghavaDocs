# Introduction
Neo4j is a graph database and analysis software

The Neo4j Browser is the main interactive tool used to create your graph analysis. It consists of the following components:
- The Editor: For command editing and execution
- Stream: For scrolling series of result frames
- Frame Code View: Viewing requests and responses
- Sidebar: Consolidates all Labels, Relationships, and Property Keys

We can create a node using:
``` CREATE (ee:Person { name: "Emil", from: "Sweden", klout: 99 }) ```
Multiple nodes can also be created by repeating the above code with different properties in a comma-separated list

We can find/match a node using:
``` MATCH (ee:Person) WHERE ee.name = "Emil" RETURN ee; ```

Pattern Matching is done using the following query:
``` 
MATCH (ee:Person)-[:KNOWS]-(friends)
WHERE ee.name = "Emil" RETURN ee, friends
```

The above pattern matching can be used to make recommendations by incorporating the return clause:
``` 
MATCH (js:Person)-[:KNOWS]-()-[:KNOWS]-(surfer)
WHERE js.name = "Johan" AND surfer.hobby = "surfing"
RETURN DISTINCT surfer
``` 

To gain a deeper understanding of how the query is working, prepend ```EXPLAIN``` or ```PROFILE``` to it