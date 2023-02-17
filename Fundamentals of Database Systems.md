# Fundamentals of Database Systems

[TOC]

# Entity-Relationship:


- ## Attributes:
	- ### Simple vs. Composite
		- Simple : Atomic attribute; cannot be broken down further
		- Composite: Can be broken down into smaller sub-parts
	- ### Single-valued vs. Multi-valued
		- Single: Each entity can have at most one value
		- Multi: Each entity can have more than one value
	- ### Stored vs. Derived
		- Stored: Must be stored in the data (cannot be inferred from other information)
		- Derived: Can be computed from other attributes (e.g. age from DOB)
	- ### Null-valued 
		- The value of an attribute is not stored nor can be derived
		- A null value will not be used in any computation
	- ### Key Attribute
		- Used to uniquely identify entities of some type
		- Its values are distinct
	
		If a given entity type does not have a key attribute, it is called a weak type.
		
		**Avoid creating new IDs for types that have natural IDs: For example, use National ID instead of Student ID, or Bank Account Number.**
- ### Example

	//Get from the Slides

- ## Relationships
	- ### What is a relationship?
		- Defines an association between two or more entities
		- Refers to an instance between objects
		- Might have one or more attributes
		- Might include more than two entities
		- **Degree** of a relationship is the number of participating entity types

	- ### Most common *cardinality* ratios for binary relationships
		- 1:1 (one to one) One person can only have one spouse
		- 1:N (one to many) One person can have more than one child
		- M:N (many to many) many people can be relatives of many people

	- ### Participation Constraint
		- Partial (Does not have to participate)
		- Total (All entities have to participate)
		
		Participation constraints can be associated with a structural constraint, specifying min/max number of entities that can exist in the relationship.
	- ### Recursive Relationship
		Between two different entities of the same type.

		Roles should be added to each participating entity so signify the roles each entity plays. For example, a supervisor employee has a supervision relationship with a supervised employee.
		
	- ### Identifying Relationships
		Weak entity types are identifies by being related to a strong entity in combination with some of their attributes.
