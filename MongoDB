Q1: What do you understand by NoSQL databases? Explain. 
At the present time, the internet is loaded with big data, big users, big complexity etc. and also becoming more complex day by day. 
NoSQL is answer of all these problems; It is not a traditional database management system, not even a relational database management system (RDBMS). 
NoSQL stands for “Not Only SQL”. NoSQL is a type of database that can handle and sort all type of unstructured, messy and complicated data. 
It is just a new way to think about the database.

Q2: What are NoSQL databases? What are the different types of NoSQL databases?
A NoSQL database provides a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases 
(like SQL, Oracle, etc.).

Types of NoSQL databases:

Document Oriented
Key Value
Graph
Column Oriented

Q3: When should we embed one document within another in MongoDB? When should we embed one document within another in MongoDB?
You should consider embedding documents for:

contains relationships between entities
One-to-many relationships
Performance reasons

Q4: What are the advantages of NoSQL over traditional RDBMS? What are the advantages of NoSQL over traditional RDBMS?
NoSQL is better than RDBMS because of the following reasons/properities of NoSQL:

It supports semi-structured data and volatile data
It does not have schema
Read/Write throughput is very high
Horizontal scalability can be achieved easily
Will support Bigdata in volumes of Terra Bytes & Peta Bytes
Provides good support for Analytic tools on top of Bigdata
Can be hosted in cheaper hardware machines
In-memory caching option is available to increase the performance of queries
Faster development life cycles for developers
Still, RDBMS is better than NoSQL for the following reasons/properties of RDBMS:

Transactions with ACID properties - Atomicity, Consistency, Isolation & Durability
Adherence to Strong Schema of data being written/read
Real time query management ( in case of data size < 10 Tera bytes )
Execution of complex queries involving join & group by clauses


Q5: Explain difference between scaling horizontally and vertically for databases?
Horizontal scaling means that you scale by adding more machines into your pool of resources whereas
Vertical scaling means that you scale by adding more power (CPU, RAM) to an existing machine.
In a database world horizontal-scaling is often based on the partitioning of the data i.e. each node contains only part of the data, 
in vertical-scaling the data resides on a single node and scaling is done through multi-core i.e. spreading the load between the CPU and RAM resources of that machine.

Good examples of horizontal scaling are Cassandra, MongoDB, Google Cloud Spanner. 
and a good example of vertical scaling is MySQL - Amazon RDS (The cloud version of MySQL).


Q6: How can you achieve primary key - foreign key relationships in MongoDB? How can you achieve primary key - foreign key relationships in MongoDB?
By default MongoDB does not support such primary key - foreign key relationships. However, we can achieve this concept 
by embedding one document inside another (aka subdocuments). Foe e.g. an address document can be embedded inside customer document.


Q7: What is Sharding in MongoDB? Explain. What is Sharding in MongoDB? Explain.
Sharding is a method for storing data across multiple machines. MongoDB uses sharding to support deployments with very large data sets and high throughput operations.



Q8: How do I perform the SQL JOIN equivalent in MongoDB? How do I perform the SQL JOIN equivalent in MongoDB?
Mongo is not a relational database, and the devs are being careful to recommend specific use cases for $lookup, 
but at least as of 3.2 doing join is now possible with MongoDB. The new $lookup operator added to the aggregation pipeline is essentially identical to a left outer join:


Q9: Does MongoDB support ACID transaction management and locking functionalities? Does MongoDB support ACID transaction management and locking functionalities?
ACID stands that any update is:

Atomic: it either fully completes or it does not
Consistent: no reader will see a "partially applied" update
Isolated: no reader will see a "dirty" read
Durable: (with the appropriate write concern)
Historically MongoDB does not support default multi-document ACID transactions (multiple-document updates that can be rolled back and are ACID-compliant). 
However, MongoDB provides atomic operation on a single document. MongoDB 4.0 will add support for multi-document transactions, making it the only database to combine the speed, 
flexibility, and power of the document model with ACID data integrity guarantees.



Q10: Explain advantages of BSON over JSON in MongoDB? Explain advantages of BSON over JSON in MongoDB?
BSON is designed to be efficient in space, but in some cases is not much more efficient than JSON. In some cases BSON uses even more space than JSON. 
The reason for this is another of the BSON design goals: traversability. BSON adds some "extra" information to documents, like length of strings and subobjects. 
This makes traversal faster.
BSON is also designed to be fast to encode and decode. For example, integers are stored as 32 (or 64) bit integers, 
so they don't need to be parsed to and from text. This uses more space than JSON for small integers, but is much faster to parse.
In addition to compactness, BSON adds additional data types unavailable in JSON, notably the BinData and Date data types.


Q11: How does column-oriented NoSQL differ from document-oriented? How does column-oriented NoSQL differ from document-oriented?
The main difference is that document stores (e.g. MongoDB and CouchDB) allow arbitrarily complex documents, i.e. subdocuments within subdocuments, 
lists with documents, etc. whereas column stores (e.g. Cassandra and HBase) only allow a fixed format, e.g. strict one-level or two-level dictionaries.
For example a document-oriented database (like MongoDB) inserts whole documents (typically JSON), whereas in Cassandra (column-oriented db) you can address 
individual columns or supercolumns, and update these individually, i.e. they work at a different level of granularity. 
Each column has its own separate timestamp/version (used to reconcile updates across the distributed cluster).

The Cassandra column values are just bytes, but can be typed as ASCII, UTF8 text, numbers, dates etc. 
You could use Cassandra as a primitive document store by inserting columns containing JSON - but you wouldn't get all the features of a real document-oriented store.


Q12: What does Document-oriented vs. Key-Value mean in context of NoSQL? What does Document-oriented vs. Key-Value mean in context of NoSQL?
A key-value store provides the simplest possible data model and is exactly what the name suggests: it's a storage system that stores values indexed by a key. 
You're limited to query by key and the values are opaque, the store doesn't know anything about them. 
This allows very fast read and write operations (a simple disk access) and I see this model as a kind of non volatile cache (i.e. well suited if you need 
fast accesses by key to long-lived data).
A document-oriented database extends the previous model and values are stored in a structured format (a document, hence the name) that the database can understand. 
For example, a document could be a blog post and the comments and the tags stored in a denormalized way. 
Since the data are transparent, the store can do more work (like indexing fields of the document) and you're not limited to query by key. 
As I hinted, such databases allows to fetch an entire page's data with a single query and are well suited for content oriented applications 
(which is why big sites like Facebook or Amazon like them).

Other kinds of NoSQL databases include column-oriented stores, graph databases and even object databases.



Q13: When should I use a NoSQL database instead of a relational database? When should I use a NoSQL database instead of a relational database?
Relational databases enforces ACID. So, you will have schema based transaction oriented data stores. It's proven and suitable for 99% of the real world applications. 
You can practically do anything with relational databases. But, there are limitations on speed and scaling when it comes to massive high availability data stores. 
For example, Google and Amazon have terabytes of data stored in big data centers. 
Querying and inserting is not performant in these scenarios because of the blocking/schema/transaction nature of the RDBMs. 
That's the reason they have implemented their own databases (actually, key-value stores) for massive performance gain and scalability.
If you need a NoSQL db you usually know about it, possible reasons are:

client wants 99.999% availability on a high traffic site.
your data makes no sense in SQL, you find yourself doing multiple JOIN queries for accessing some piece of information.
you are breaking the relational model, you have CLOBs that store denormalized data and you generate external indexes to search that data.


Q14: When would you use NoSQL? When would you use NoSQL?
It depends from some general points:

NoSQL is typically good for unstructured/"schemaless" data - usually, you don't need to explicitly define your schema up front and can just include new fields without any ceremony
NoSQL typically favours a denormalised schema due to no support for JOINs per the RDBMS world. So you would usually have a flattened, denormalized representation of your data.
Using NoSQL doesn't mean you could lose data. Different DBs have different strategies. e.g. MongoDB - you can essentially choose what level to trade off performance vs potential for data loss - best performance = greater scope for data loss.
It's often very easy to scale out NoSQL solutions. Adding more nodes to replicate data to is one way to a) offer more scalability and b) offer more protection against data loss if one node goes down. But again, depends on the NoSQL DB/configuration. NoSQL does not necessarily mean "data loss" like you infer.
IMHO, complex/dynamic queries/reporting are best served from an RDBMS. Often the query functionality for a NoSQL DB is limited.
It doesn't have to be a 1 or the other choice. My experience has been using RDBMS in conjunction with NoSQL for certain use cases.
NoSQL DBs often lack the ability to perform atomic operations across multiple "tables".


Q15: What is Denormalization? What is Denormalization?
It is the process of improving the performance of the database by adding redundant data.



Q16: Define ACID Properties Define ACID Properties
Atomicity: It ensures all-or-none rule for database modifications.
Consistency: Data values are consistent across the database.
Isolation: Two transactions are said to be independent of one another.
Durability: Data is not lost even at the time of server failure.


Q17: How does MongoDB ensure high availability? How does MongoDB ensure high availability?
Q18: MongoDB relationships. What to use - embed or reference? MongoDB relationships. What to use - embed or reference?
Q:I want to design a question structure with some comments, but I don't know which relationship to use for comments: embed or reference? 
Explain me pros and cons of both solutions?

Q19: Explain use of transactions in NoSQL Explain use of transactions in NoSQL
Q20: How do you track record relations in NoSQL? How do you track record relations in NoSQL?
Q21: Explain eventual consistency in context of NoSQL Explain eventual consistency in context of NoSQL
Q22: Explain how would you keep document change history in NoSQL DB? Explain how would you keep document change history in NoSQL DB?
Q23: Explain BASE terminology in a context of NoSQL Explain BASE terminology in a context of NoSQL
Q24: Where does MongoDB stand in the CAP theorem? Where does MongoDB stand in the CAP theorem?
Q25: Explain the differences in conceptual data design with NoSQL databases? Explain the differences in conceptual data design with NoSQL databases?











