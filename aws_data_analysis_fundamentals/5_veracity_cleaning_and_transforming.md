# Veracity – cleansing and transformation

- When you have data that is ungoverned, coming from numerous, dissimilar systems and cannot curate the data in meaningful ways, you know you have a veracity problem.
- **Curation** is the action or process of selecting, organizing, and looking after the items in a collection.
- **Data integrity** is the maintenance and assurance of the accuracy and consistency of data over its entire lifecycle.
- **Data veracity** is the degree to which data is accurate, precise, and trusted.
- Data veracity is contingent on the integrity of the data. We will discuss the specifics of data integrity in the next topic.

- not all data is generated equally
- data integrity
  - creation: ensuring data accuracy when data is created, regular audits might be necessary
  - aggregation: key phase for many systems, loss of integrity in this phase might due to planning
  - storage: maintaining data in secure form, some data is subject to frequent change, and some are stable
  - access: your data is visible to users, data's integrity cannot change, here it is mostly read only
  - sharing: once report has been created they are shared with businesses, read only here too.

**Data cleansing** is the process of detecting and correcting corruptions within data.
**Referential integrity** is the process of ensuring that the constraints of table relationships are enforced.
**Domain integrity** is the process of ensuring that the data being entered into a field matches the data type defined for that field..
**Entity integrity** is the process of ensuring that the values stored within a field match the constraints defined for that field.


### What does clean look like?
Before you do anything else, you must come to a consensus on what clean looks like. Some businesses deem clean data to be data in its raw format with business rules applied. Some businesses deem clean data as data that has been normalized, aggregated, and had value substitutions applied to regulate all entries. These are two very different understandings of clean. Be sure to know which one you are aiming for.

### Where are the errors coming from? 
As you find errors in the data, trace them back to their likely source. This will help you to predict workloads that will have integrity issues. It will also help you make a case for changes to the system that would improve the efficiency of the ETL operations.

### Know what acceptable changes look like
From a purely data-centric view, entering a zero in an empty column may seem like an easy data cleansing decision to make, but beware the effects of this change. Likewise, combining the "On Order" and "In Stock" inventory numbers for monthly reports may seem inconsequential. However, that data may wind up in the hands of an inventory manager who now believes that there is an inventory loss problem. These are the small details that can make a huge, negative impact.

### Know if original data has value
In some systems, the original data is no longer valuable once it has been transformed. However, in highly regulated data or highly volatile data, it is important that both the original data and the transformed data are maintained in the destination system.

For example, in an online gaming system, there may be no value in recording every direction shift a player makes as they are moving on the map. The only important value is when the player enters or exits key areas of the map. However, in a banking app, all details of every transaction are vital for auditing, even though a customer may only care to see if their transaction was successful or not.

- ACID is an acronym for Atomicity, Consistency, Isolation, and Durability. It is a method for maintaining consistency and integrity in a structured database.
- BASE is an acronym for Basically Available Soft state Eventually consistent. It is a method for maintaining consistency and integrity in a structured or semistructured database.

| ACID compliance                         | BASE compliance                      |
| --------------------------------------- | ------------------------------------ |
| Strong consistency                      | Weak consistency – stale data is OK  |
| Isolation is key                        | Availability is key                  |
| Focus on committed results              | Best effort results                  |
| Conservative (pessimistic) availability | Aggressive (optimistic) availability |

### Amazon DynamoDB transactions
- This feature implements ACID compliance across one or more tables within a single AWS account and region.


ETL—Extract, Transform, Load—is the process of collecting data from raw data sources and transforming that data into a common type. This new data is loaded into a final location to be available for analytical analysis and inspection. In modern cloud-based environments, we often refer to this process as ELT (Extract, Load, Transform) instead. The steps are simply performed in a different order, but the result is the same.

________

## Amazon EMR
- hands on approach to creating data pipeline
- robust data collection and processing platform
- requires strong technical knowledge

## AWS Glue
- serverless, managed ETL
- great for simple ETL
- can be used as a metastore using AWS Glue data catalog
- which is a drop in replacement for Hive metastore

- denormalization might be part of the ETL process
