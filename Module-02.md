# Module 2: General PHP Programming

Prior to completing the module below it is highly recommended that you look at the following learning material.  Note that the content here is PHP 5.4+ specific.

* [PHP The Right Way](http://phptherightway.com)


## The Test


### 1. Variables, Constants and Strings

1. Create a new git repo in your GitLab account under your namespace called `PHP`, all the code for this module should be commited there.
2. Create a file called `constants.php` and define 5 PHP constants there. Via the `define()` method. Assign some constants string values and some integer values. The integer values should be between 1 and 5.
3. => Stage, commit and push your changes to GitLab.
4. Create a new file called `main.php`.  In the `main.php` file bring in the constants.php file in a way that will make it required and that it will be brought in only one time.
5. Now create an array variable called `array` and assign it an associative array, using key names that are string constants from your constants.php file and at least 1 value that is an integer constant from constants.php.
6. Now create an integer variable called `result` and assign it the output of the multiplication of 2 or more array values.  In this equation you should use array keys that are constants defined in constants.php.
7. Now print out the result as a string in the format of:  "The result of X * Y is: Z". Create this message WITHOUT string concatenation and without re-assigning any new variables.
8. => Stage, commit and push your changes in GIT.
9. Now refactor the printed string to use string concatenation.
10. => Stage, commit and push your changes in GIT.
11. Create a new string variable that holds 3 multi-line paragraphs of text, this text can be anything you want and should have at least 5 variable substitutions within the string.  You can create the variables to put into this string if necessary.  Do not use string concatenation or a multi-line string inside double quotes to create the string's value.  Print the string's value.
12. => Stage, commit and push your changes to GitLab.

### 2. Loops & Control Structures

1.  Create a new file called loop-control.php and inside create an array called `numbers` which contains integer values between `0` and `100` with a step of `3` between each number, i.e. `0, 3, 6, 9, 12` etc..  Do this with the least amount of code you can.
2.  Now create a `foreach` loop to iterate over the array, inside the `foreach` loop add logic to do the following *without* using an `if-else` statement:  
	a.  If the number is 3 print "Three" one time.
	b. 	If the number is 9 print "Nine" 3 times.
	c.	If the number is 15 print "Fifteen" 5 times
3.  => Stage, commit and push your changes to GitLab.
4.  Now refactor the logic inside the `foreach` loop to do the following: (`if` and `else` can be used now)
	a. If the number is a multiple of `7` print out "Sevens are lucky, this number has X", where X is the number multiples of `7` represented by the number.
	b.  Otherwise if the number is a multiple of `10` print out "X is a round number" where X is the number.
	c.  If the number is the first in the group print out "First number"
	d.  If the number is the last in the group print out "Last number"
5.  => Stage, commit and push your changes to GitLab.
6.  Refactor the code to be a for loop.
7.  => Stage, commit and push your changes to GitLab.
8.  Refactor the code to be a while loop.
9.  => Stage, commit and push your changes to GitLab.
10.  Refactor the code to be a do-while loop.
11.  => Stage, commit and push your changes to GitLab.

### 3. Functions

1.  Create a new file called `functions.php`
2.  Create 4 math functions: `add`, `subtract`, `multiply` and `divide` 2 given parameters. 
3.  Use all of the functions and print out the result, show how you would pass arguments to the functions by value and by reference.
4.  Create a function which takes 2 comparison parameters and a 3rd boolean parameter defaulting to false, which tells the function whether or not to compare the data type as well.  Have the function print out a string that tells if the parameters are equal or not, and if they are equal in datatype if the 3rd parameter was true.
5.  Use the comparison function and pass in the following parameters:
	a.  4, "4"
	b.  5, "5", true
	c.  4, 4.0
	d.  5. 5.0, true
6. => Stage, commit and push your changes to GitLab.

### 4. Classes

1.	Create a new class called Math in a file named `math.php` and copy your previous 4 math functions into the class as public functions.
2.  Refactor each function so it will be able to take a minimum of `2` integer paramaters with no maximum number of parameters.  I.E. You could pass in `2` arguments or `n`.  The functions should return the relevant operation applied to all the function arguments, in the order they were given.
3.  Create a new file called do_math.php which uses each function in the Math class 3 times and prints out the output.
4.  => Stage, commit and push your changes to GitLab.
5.  Now refactor your `Math` class to have 4 constants that represent each math operation and a private method called `doOperation` who's first parameter is the type of operation to do and subsequent parameters are the values to do that operation on. Then refactor the previous functions to all use the new `doOperation` function.
6.  => Stage, commit and push your changes to GitLab.

### 5. Inheritance, Interfaces, Namespaces and Traits

	Create a new branch in your PHP git repository called `advanced` and push your code for the following exercises there.  Place all the following code in a folder called `advanced`.

1.  Create an interitance hirarchy composed of 7 classes:

	a.  Computer > Workstation
	b.  Workstation > Mac
	c.  Workstation > PC
	d.  Computer > Server
	e.	Server > WebServer
	f. 	Server > DatabaseServer
	
Create a new PHP file called `main.php` which uses these classes. Be creative and show the following concepts (you can simiply echo strings for the function logic):

1.  Public, Protected and Private functions
2.  Public, Protected and Private properties
3.  Overwriting inherited functions
4.  Overwriting inherited functions but still executing the parent's functionality for that function before implementing the child's logic.
5.  => Stage, commit and push your code to GitLab.
6.  Refactor your code to show the use of namespaces using the keywords "use" and "as"
7.  => Stage, commit and push your code to GitLab.
8.  Now refactor your code to use at least one `interface`.
9.  => Stage, commit and push your code to GitLab.
10. Now refactor your code to include at least one `trait` which should contain a function that executes then extends a super class's functionality.
11. => Stage, commit and push your code to GitLab.
12. Now refactor your code to include at least 3 `closures`, if your code already has this, add 3 more.
13. => Stage, commit and push your code to GIT **with a commit message of `closures`**


### 6. Final

**Create a new Git Repo in your GitLab namespace called `php-final` and put all your code for the following exercise there.**

Create a simple PHP application **that does not use an existing framework or 3rd party libraries** and has the characteristics listed below.

**Note that this execrcise should be kept as simple as possible, do not develop beyond the feature requirements below.**

1.  Uses the MVC design pattern (limit to 1 model and 1 controller for simplicity)
2.  Uses a namespace
4.  Saves information into a MySQL database
5.  Illustrates Create, Read, Update and Delete functions on a Model (all database interaction should happen at the model layer)
6.  Has static methods on the model for `find()` and `findAll()` for fetching model records.
7.  Inserts or updates a record into the database using a `save()` method on the Model.
8.  Deletes the record from the database using a `destroy()` method on the Model.
9.  Validates properties on the model using a `validate()` function which returns `true` or `false` as to whether or not the model is valid.
10.  The model's `validate()` function should feed data to an `errors()` function that returns an array of errors if any.
11.  The model's `save` function should return `true` or `false` if a `insert` or `update` was successful, and should validate the model prior to attempting to save.  If the model is invalid the `save()` should not complete and should return `false`.
12.  If a model does not save for some reason the user should be returned to the Create or Update view and be shown the errors.

### Wrapping Up

When you are done with all the exercises you should have 2 git repositories in your personal GitLab namespace ('PHP' and 'php-final').  Please create a tag in each of these repos called `v1.2` with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in GitLab, then add Brian Webb to both repos with "Developer" permissions.  


Any required communication will again be done on the "issues" feature for the project so this feature **MUST** be enabled in the settings for each repo.  Once your work from this module has been accepted move on to the next module.  You **can** move on to the next module prior to approval, but be aware that some modules build on others output so you may be creating more work for yourself if one module's output needs modification to be accepted.