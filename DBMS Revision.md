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

Horizontal - make servers powerful - network calls - one machine fails then others present - no limit

Vertical - add more servers - interprocess communications - one machine fails then no redirections - limit

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
1NF - no multi valued attributes(C1,C2)
2NF - 1NF + no partial depencies (id, course fee, course no present & course fee is dependent on course no which is non prime)
3NF - 2NF + no transitive dependency (id -> state -> country)
BCNF - 3NF + LHS is PK (A -> B then A is primary key)

## denormalization 

- adding redundant data to avoid costly joins 
- not equal to reversing normalization 
- generally applied after normalization 
- (tb1 = course, tb2 = teacher name, details, we need to join them every time. so instead we add teacher name to tb1 too)

## Functional dependency 
variables are functionally dependent
X -> Y where X=determinant, Y=dependent
