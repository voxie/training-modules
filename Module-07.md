# Module 7: Architecture

***

## Getting Started

Prior to completing the module below it is highly recommended that you familiarize yourself with the following learning material:
- [Basic Database Normalization](http://databases.about.com/od/specificproducts/a/normalization.htm)
- [Practical Normalization](http://support.microsoft.com/kb/283878)
- [More on Normalization](http://en.wikipedia.org/wiki/Database_normalization)
- [Real World Normalization Perspective](http://www.codinghorror.com/blog/2008/07/maybe-normalizing-isnt-normal.html)
- [ActiveRecord Design Pattern](https://en.wikipedia.org/wiki/Active_record_pattern)
- [Eloquent Model Conventions](http://laravel.com/docs/master/eloquent#defining-models)
- [Entity-Relationship Model > Crows Foot Notation](https://en.wikipedia.org/wiki/Entity–relationship_model#Crow.27s_Foot_Notation)

***

## Completing the module

1. Create a new branch in your 'php-final' git repo called `architecture` and commit all the work from this module there.
2. Following the Laravel conventions and patterns for database architectures, create an Entity Relationship Diagram (ERD) using Crow's Foot Notation to diagram the Entities and Relationships below.
3. Use whatever attributes you think are necessary for each Entity. Be sure to include necessary "timestamp" attributes for each Entity to conform to the Laravel standard.
4. Use whatever diagramming tool you like. You could even draw it and take a picture if you like, as long as the diagram is clear.

### Company

- belongs to: Company Type
- has and belongs to many: Users
- has many companies
- belongs to (0 or 1 Company)

### Company Type

- has many: Companies

### User

- has and belongs to many: Companies
- has and belongs to many: User Types per company
- has one User: Status

### User Status

- has many: Users

***

## Wrapping Up

When you are done, push your code to GitHub. Please create a tag called `v1.7` with a message of `"ready for review"`.  Be sure your tags are pushed to the remote repository and are visible in GitHub.

Create an issue titled **Review Module 7 - Architecture** and assign it to [**@generationtux-helmsmen**](https://github.com/generationtux-helmsmen).
