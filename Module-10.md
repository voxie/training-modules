# Module 10: Reusable Code in Packages

***

## Getting Started

Creating packages to hold reusable code is a very important practice. For this task you will need to build a GUI package that has self-contained functionality. It should have the ability to be used in your existing Laravel application which is where you'll need to show its implementation.

Create a new branch in your Bitbucket 'Laravel-Test' repo called `package` and commit all the work from this module there.

***

## The Test

### Test Requirements

1. Should contain a [Laravel service provider](http://laravel.com/docs/master/packages) for Laravel integration.
2. Your package should use template or "partial" files to contain the HTML for each GUI element. This will allow you to later update the HTML if needed.
3. Your package should provide static functions that can be used in your views. The functions should accept data objects or values and output the appropriate GUI element with the data contained in it.

Example blade view code (note: you don't have to use these namespaces and class names, they are just for example):

_Now would be a good time to review the difference between `{{` and `{!!` in Blade._

````
{!! \Indatus\GuiLibrary\Table::summary($multiDimArray, $options); !!}
{!! \Indatus\GuiLibrary\Button::normal('click me', $target); !!}
{!! \Indatus\GuiLibrary\Link::normal('link to something', $target); !!}
````

### Required GUI Elements

1. **Table**: Should accept a multi-dimensional array with key-names as columns. Additionally the table component should accept some other arguments that format the table as you choose.
2. **Dropdown**: Should accept an array of key-values for the options list and some way to indicate the selected element if an item is to be selected.
3. **Link**: Should accept the link text, link target and options.
4. **Textfield**: Should accept name and data to display as well as options.
5. **Label**: Should accept text content and "for" attribute as well as options.

### Other Items

1. **Assets**: Your package should contain at least one (1) CSS stylesheet and one (1) Javascript file. The implementation of the Javascript and CSS is up to you.
2. **Asset Methods**: Your package should include at least two (2) static methods that output the necessary stylesheets and Javascript for inclusion in view or layout files. For example you may have code like:
  ````
  <html>
    <head>
      <title>Test</title>
      {!! \Indatus\GuiLibrary\Asset::container('mypackage')->styles(); !!}
      {!! \Indatus\GuiLibrary\Asset::container('mypackage')->scripts(); !!}
    </head>
  ````
3. **README**: Your package must include a `README.md` file written in Markdown syntax that includes documentation on how to install your package as well as code usage examples.

### Displaying Your Work

1. Create a new view in your Laravel app at the URI /package which will render an HTML view that displays an example of each GUI component you've created.

***

## Wrapping Up

When you are done, push your code to Bitbucket. Please create a tag called `v2.0` with a message of `"ready for review"`. Be sure your tags are pushed to the remote repository and are visible in Bitbucket.

Create an issue titled **Review Module 10 - Reusable Code in Packages** and `@mention` your mentor and team leader.
