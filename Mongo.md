# Basic Usage - 3.2.3

## Installation

[Link](https://www.howtoforge.com/tutorial/install-mongodb-on-ubuntu-16.04/)

## Commands

- See Current Working Database - `db`
- List Databases       - `show dbs` or `show databases`
- List Collections     - `show databases`
- Select Database - `use foobar_db`


### Create(C)
	
	> post = {title : "First Post", author: "Ivory4491"}
	{
		"title" : "First Post",
		"autor" : "Ivory4491"
	}
	> db.posts.insert(post)
	WriteResult({ "nInserted" : 1 })


### Read(R)
	
	> db.posts.find()
	{
		"_id" : ObjectId("573c7dcd48245fa02f616610"),
		"title" : "First Post",
		"autor" : "Ivory4491"
	}
	> db.posts.findOne()
	{
		"_id" : ObjectId("573c7dcd48245fa02f616610"),
		"title" : "First Post",
		"autor" : "Ivory4491"
	}


### Update(U)

	> post.tags = []
	[ ]
	> db.posts.update({title: "First Post"}, post)
	WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })

	> db.posts.find()
	{
		"_id" : ObjectId("573c7dcd48245fa02f616610"),
		"title" : "First Post",
		"tags" : [ ],
		"autor" : "Ivory4491"
	}


### Delete(D)

	> db.posts.remove({tags: []})
	WriteResult({ "nRemoved" : 1 })
	> db.posts.find()


## ObjectId(_id)

	
- Every document have an "_id" key
- ObjectIds use 12 bytes of storage
- Default **ObjectIds** have **24** hexadecimal digits
	
	- 4-byte - The seconds since the Unix epoch
	- 3-byte - Machine identifier
	- 2-byte - Process ID (PID)
	- 3-byte - Random Value

	
