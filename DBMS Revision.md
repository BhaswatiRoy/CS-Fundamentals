## ACID Properties

![image](https://user-images.githubusercontent.com/78029145/221472702-85640401-ca1f-4f14-8a32-f91f1ed62b2f.png)

## Types of SQL Languages

![image](https://user-images.githubusercontent.com/78029145/221472770-62cd64e0-79c5-4fe1-93f7-ec0ebfffc2f9.png)

DDL - CREATE, DROP, TRUNCATE, ALTER, RENAME

DQL - SELECT

DML - INSERT, UPDATE, DELETE, LOCK(restrict controls)

DCL - GRANT, REVOKE

TCL - COMMIT, ROLLBACK

## Horizontal Scaling vs Vertical Scaling

Horizontal (scaling out) - make servers powerful - network calls - one machine fails then no redirections

Vertical (scaling up) - add more servers - interprocess communications - one machine fails then others present

## Horizontal Partitioning vs Vertical Partitioning

horizontal partitioning/db sharding - divide tables on basis of rows

vertical partitioning - divide tables on basis of cols using primary or foreign keys

## Types of Keys

![image](https://user-images.githubusercontent.com/78029145/221472975-800fab66-8f87-42b3-bcbd-0830b244dc4a.png)

## Types of Relationships

![image](https://user-images.githubusercontent.com/78029145/221472999-34ce615f-2152-430b-bd29-d8976c9e7ccb.png)

## 3 Schema Architecture or 3 Levels of Abstraction

1. external/view level - normal users can view - work of fronend
2. conceptual/logical level - structure of db stored - work of db designing
3. physical/internal level - actual loc of db - work of backend

## Normalization 

removal of data redundancy 
- 1NF - no multi valued attributes(C1,C2)
- 2NF - 1NF + no partial depencies (id, course fee, course no present & course fee is dependent on course no which is non prime)
- 3NF - 2NF + no transitive dependency (id -> state -> country)
- BCNF - 3NF + LHS is PK (A -> B then A is primary key)

## Denormalization 

- adding redundant data to avoid costly joins 
- not equal to reversing normalization 
- generally applied after normalization 
- (tb1 = course, tb2 = teacher name, details, we need to join them every time. so instead we add teacher name to tb1 too)

## Functional Dependency 

variables are functionally dependent

X -> Y where X=determinant, Y=dependent

## ER Diagram

![image](https://user-images.githubusercontent.com/78029145/221473490-4a5c2bb2-3275-4694-a038-cbb1c870ba02.png)

logical overview of a database system and has entity(rectangle) & attributes(oval)

1. key attributes = uniquely define themselves like rollno
2. composite attributes = combo of many attributes like address->street+city+state+country
3. multivalued attributes = has more than 1 value like phone no
4. derived attributes = can be derived from other attributes like age derived from dob

## Relationship 

relation between entities (enrolled is relation between student & course entity) (diamond)
1. unary = one entity (person married to another person only)
2. binary = two entities (student enrolled in courses)
3. n ary = n entities (car trees people building living in a city)

## Cardinality of Relationship

1. one to one
2. one to many
3. many to many

## Serializability 

check which schedules are serializable means they can be arranged in a serial order to perform

- conflict serializability - schedule can be made serial using conflict eq method (moving processes up & down - swap non conflict pairs)

- view serializability - schedule that gives same calculation values for both actual & serial forms (calculate math operations like A=A-20 etc)

## Concurrency Control Protocols 

protocols to smoothly execute concurrent db processes and make sure recoverability & serializability is maintained

1. Lock Based - 

A. Shared & Exclusive locks -
shared lock (locked transaction is allowed to read only) & exclusive     lock (locked transaction is allowed to read & write)

B. 2 Phase Locking Protocol -
growing (locks acquired) & shrinking (locks released)
types - strict 2pl (2pl+all exclusive locks should hold until commit/abort), rigorous 2pl (2pl+all shared & exclusive locks should hold until commit/abort)

2. Timestamp Ordering Protocol -

latest transactions get executed first

A. Read TS    

B. Write TS

## Strong Entity vs Weak Entity & Entity Set

strong entity - can uniquely identify themselves like id no
weak entity - can not uniquely identify themselves like course name
entity set - collection of entities of same type

## Types of Joins

1. Inner join - common data 
2. Natural join - same as inner join but don't keep duplicates
3. Outer join - 1 table + common data
      A. Left outer join - left table + common
      B. Right outer join - right table + common
4. Full join - both tables


## 2 Tier vs 3 Tier Architecture

![image](https://user-images.githubusercontent.com/78029145/221476894-be1e0db9-dd7f-415b-8333-068572cd6f72.png)


## DELETE vs TRUNCATE

DELETE - remove data not table/ dml/ slower/ more transaction space

TRUNCATE - remove entire table/ ddl/ faster/ less transaction space




