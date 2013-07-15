# Module 7: Architecture

Prior to completing the module below it is highly recommended that you look at the following learning material.  

* [Basic Database Normalization](http://databases.about.com/od/specificproducts/a/normalization.htm)
* [Practical Normalization](http://support.microsoft.com/kb/283878)
* [More on Normalization](http://www.princeton.edu/~achaney/tmve/wiki100k/docs/Database_normalization.html)
* [Real World Normalization Perspective](http://www.codinghorror.com/blog/2008/07/maybe-normalizing-isnt-normal.html)
* [ActiveRecord Design Pattern](https://en.wikipedia.org/wiki/Active_record_pattern)
* [Laravel's Eloquent ORM: Basic Usage (naming conventions)](http://laravel.com/docs/eloquent#basic-usage)
* [Entity-Relationship Model > Crows Foot Notation](https://en.wikipedia.org/wiki/Entity–relationship_model#Crow.27s_Foot_Notation)
* [Indatus Laravel Dev Standards,  See: Migrations / Database](http://helpdesk.indatus.com/KB/a198/laravel-php-framework-development-standards.aspx)


## The Test


Create a new branch in your 'php-final' git repo called 'architecture' and commit all the work from this module there. 

Following the Laravel conventions and patterns for database architectures create an Entity Relationship Diagram (ERD) using Crow's Foot Notation to diagram the Entities and Relationships below.  Be creative and create whatever attributes you think are necessary for each Entity.  Be sure to include necessary "timestamp" attributes for each Entity to conform to the Laravel standard.  Use whatever diagramming tool you like, you could even draw it and take a picture if you like as long as the diagram is clear.

	
1.  Company

	a. belongs to: Company Type
	b. has and belongs to many: Users
	c. has many companies
	d. belongs to (0 or 1 Company)
	
2.  Company Type

	a. has many: Companies
	
3.  User

	a. has and belongs to many: Companies
	b. has and belongs to many: User Types per company
	c. has one: User Status
	
4.  User Status

	a. has many: Users

	 



----------

When you are done, push your code to GIT under this branch, then merge this branch back into 'master' (but don't delete this branch).  Please create a tag called **v1.7** with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in GitLab.

Any required communication will again be done on the "wall" for the project so this feature **MUST** be enabled in the settings for each repo.  Once your work from this module has been accepted you'll a) receive credit for completing this module and b) get access to start the next module.



