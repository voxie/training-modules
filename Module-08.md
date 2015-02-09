# Module 8: Laravel PHP Framework

Prior to completing the module below it is highly recommended that you look at the following learning material.  **Even if you consider yourself a Laravel expert, there is material in the resources below that even seasoned users are not aware of.  It only helps you more.**

* [What's new in Laravel 4](https://tutsplus.com/course/whats-new-in-laravel-4/)
* [Custom Artisan Commands](https://tutsplus.com/course/custom-artisan-commands-and-you/)
* [How to write testable and maintainable code in PHP](http://net.tutsplus.com/tutorials/php/how-to-write-testable-and-maintainable-code-in-php/)
* [Easier testing with Mockery](https://tutsplus.com/tutorial/easier-testing-with-mockery/)
* [Testing like a boss with Laravel models](http://net.tutsplus.com/tutorials/php/testing-like-a-boss-in-laravel-models/)
* [Better testing in Laravel](https://tutsplus.com/tutorial/better-testing-in-laravel/)
* [Modern testing with PHP in codeception](https://tutsplus.com/course/modern-testing-in-php-with-codeception/)
* [Indatus Laravel framework development standards](http://helpdesk.indatus.com/KB/a198/laravel-php-framework-development-standards.aspx)



## The Test


Create a new repository in your GitLab namespace called 'Laravel-Test' and commit all the work from this module there. 

Build a Laravel application with the features, functions, entities etc of your choosing as long as the application meets the criteria below.  Be creative and resourceful but at the same time don't take 10 years to build your app.

#### Application Criteria

**When your building your application and meeting a specific criteria below you should use a relevant commit message to indicate that your commit is satisfying a particular criteria.**

1.  Build your features using Test First Development, don't write any feature code until the failing test is created first.  Write the test, write code to make it pass, then refactor.  Rinse & Repeat. Keep in mind however that you CAN overtest your application, see: [Test like the TSA by DHH](http://37signals.com/svn/posts/3159-testing-like-the-tsa)

2.  Use Codeception to build your tests with where it accells, but you can also use PHPUnit with Laravel helpers and other testing packages that make testing easier and faster.

3.  **Follow the [Indatus Laravel framework development standards](https://docstack.io/docs/45)**.  There is a lot of requirements that will guide your development here.

4.  Integrate user authentication

5.  Integrate sending email (with HTML and Plain Text versions of the email)

6.  All your models should have validation.  Between all your models make sure you use **all** of these validation rules at least once:

	a.  Required
	b.  Numeric
	c.  Required If
	d.  Regex
	e.  Email
	f.	Url
	g.  Use a custom error message
	h.  Custom validation rule
	
7.  All models should account for mass-assignment vulnerabilities by using the `fillable` or `guarded` properties.

8.  Make sure your application is protected from the following security vulnerabilities.  The framework may or may not handle some of this for you, verify to be sure.

	a.  XSS
	b.  SQL-Injection
	c.  CSRF
	d.  Session-Fixation

9.  Include a minimum of 4 different Entities (excluding lookups).

10. Include the following relationships:

	a.  At least 1 relationship for each model
	b.  1+ belongs to relationship
	c.  1+ has many relationship
	d.  1+ has one relationship
	e.  1+ has and belongs to many relationship
	f.  1+ polymorphic relationship
	
11.  CRUD interface for at least 1 model.

12.  Handle uploading an image that is a property of an entity.  (something like `$user->avatar`).  Have 1+ alternative image representations created from the uploaded image (i.e. thumbnail etc.).  You may consider using 1 or more packages to help do this.

13.  Include at least 2 'resourceful' routes and controllers.

14.  Subscribe to at least one event.  This can be a built in event or a custom event you fire.

15.  Create at least one Facade.

16.  Use pagination at least once.

17.  Use 2+ Queues, 1 for sending email (in #5) and one custom queue.

18.  Use at least one query scope in your application.




----------

When you are done, push your code to GitLab.  Please create a tag called **v1.8** with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in GitLab.

Any required communication will again be done on the "issues" feature for the project so this feature **MUST** be enabled in the settings for each repo.  Create an issue titled "Review Module 8 - Laravel PHP Framework" and mention all team leaders and department manager.