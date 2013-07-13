#PHP Learning Module Test

Prior to completing the module below it is highly recommended that you look at the following learning material.

* [PHP The Right Way](http://phptherightway.com)


## The Test

1. Create a new git repo in your GitLab account under your namespace called PHP, all the code for this module should be commited there.
2. Create a file called constants.php and define 5 PHP constants there. Via the `define()` method. Assign some constants string values and some integer values. The integer values should be between 1 and 5.
3. => Stage, commit and push your changes to GIT.
4. Create a new file called main.php.  In the main.php file bring in the constants.php file in a way that will make it required and that it will be brought in only one time.
5. Now create an array variable called 'array' and assign it an associative array, using key names that are string constants from your constants.php file.
6. Now create an integer variable called 'result' and assign it the output of the multiplication of 2 array values.  In this equation you should use array keys that are constants defined in constants.php.
7. Now print out the result as a string in the format of:  "The result of X * Y is: Z". Create this message WITHOUT string concatenation.
8. => Stage, commit and push your changes in GIT.
9. Now refactor the printed string to use string concatenation.
10. => Stage, commit and push your changes in GIT.
11. 