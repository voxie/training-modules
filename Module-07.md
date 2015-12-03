# Module 7: Architecture

Prior to completing the module below it is highly recommended that you look at the following learning material.  

* [Basic Database Normalization](http://databases.about.com/od/specificproducts/a/normalization.htm)
* [Practical Normalization](http://support.microsoft.com/kb/283878)
* [More on Normalization](http://en.wikipedia.org/wiki/Database_normalization)
* [Real World Normalization Perspective](http://www.codinghorror.com/blog/2008/07/maybe-normalizing-isnt-normal.html)
* [ActiveRecord Design Pattern](https://en.wikipedia.org/wiki/Active_record_pattern)
* [Eloquent Model Conventions](http://laravel.com/docs/master/eloquent#defining-models)
* [Entity-Relationship Model > Crows Foot Notation](https://en.wikipedia.org/wiki/Entity–relationship_model#Crow.27s_Foot_Notation)


## The Test


Create a new branch in your 'php-final' git repo called 'architecture' and commit all the work from this module there. 

Following the Laravel conventions and patterns for database architectures create an Entity Relationship Diagram (ERD) using Crow's Foot Notation to diagram the Entities and Relationships below.  

Be creative and use whatever attributes you think are necessary for each Entity.  Be sure to include necessary "timestamp" attributes for each Entity to conform to the Laravel standard.  

Use whatever diagramming tool you like, you could even draw it and take a picture if you like as long as the diagram is clear.

	
1.  **Company**

	a. belongs to: Company Type
	b. has and belongs to many: Users
	c. has many companies
	d. belongs to (0 or 1 Company)
	
2.  **Company Type**

	a. has many: Companies
	
3.  **User**

	a. has and belongs to many: Companies
	b. has and belongs to many: User Types per company
	c. has one: User Status
	
4.  **User Status**

	a. has many: Users

	 



----------

When you are done, push your code / files to Bitbucket.  Please create a tag called `v1.7` with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in Bitbucket.

Create an issue titled **Review Module 7 - Architecture** and @mention all team leaders and department head.
