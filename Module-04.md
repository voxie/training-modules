# Module 4: Testing in PHP

Prior to completing the module below it is highly recommended that you look at the following learning material.  

* [Test-Driven PHP](http://net.tutsplus.com/sessions/test-driven-php/) (all sub articles)
* [How to Write Testable and Maintainable Code in PHP](http://net.tutsplus.com/tutorials/php/how-to-write-testable-and-maintainable-code-in-php/)
* [Easier Testing With Mockery](https://tutsplus.com/tutorial/easier-testing-with-mockery/)


## The Test

Create a new branch in your 'php-final' git repo called 'TDD' and commit all the work from this module there.

Be sure to write your code to conform to the PSR-2 spec.

1.  Use composer to install Mockery, PHPUnit and fzaninotto/Faker, your composer.json and composer.lock files should be part of this project.
2.  Add a folder called 'tests' where all your test code will go
3.  Add a test class for your previous model
4.  Add a method to the test class to test model validation, use Faker to set properties
	a. create a new object and assert that validation initially fails
	b. assert that an error exists for each particular property where validation is failing.
	c. one by one set each required poperty correctly and assert that the error does not exist.
	d. when all required properties are set assert that vaildation passes.
5.  Add a method that tests that the model's `save()` and `destroy()` methods are inserting, updating and deleting in the database correctly
	a.  assert that the model's database table is empty, or notes the number of records
	b.  create a new object, popuplate the properties with Faker and call `save()`, assert that the record was inserted into the database.
	c.  update the object and call `save()`, assert that the data in relevant table row has been updated correctly AND that no additional records were inserted.
	d.  call the `destroy()` method on the model and assert that the record has been removed from the database table.
6.  Refactor your Model's code to use dependency injection and the Repository pattern:
	a.  Following the Repository pattern add a database access object, and define an interface that speficices the methods and properties required.
	b.  Refactor your model to use dependency injection and the database access object.
	c.  Add a mock database access object that uses Mockery and conforms to the database access interface to return mock data.
7.  Add a new test method to your test class that injects the mock database access object.  Test the create, find, update and delete functionality of your model without actually hitting the database.

----------

When you are done, push your code to GIT under this branch, then merge this branch back into 'master' (but don't delete this branch).  Please create a tag called **v1.4** with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in GitLab.

Any required communication will again be done on the "wall" for the project so this feature **MUST** be enabled in the settings for each repo.  Once your work from this module has been accepted move on to the next module.  You **can** move on to the next module prior to approval, but be aware that some modules build on others output so you may be creating more work for yourself if one module's output needs modification to be accepted.


