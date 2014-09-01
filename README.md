PageTableExtended
=================

Extends the Processwire PageTable field for rendering table row layouts. This is great for editors, because they actually see at a glance what the table rows consist of.

What it does
------------

Turns the Processwire Fieldtype "Page Table" from this:

![PageTable before](http://siebennull.com/github/git1.jpg)

into something like this:

![PageTable before](http://siebennull.com/github/git2.jpg)

## Requirements

* FieldtypePageTable installed (part of the core since Processwire 2.4.10.)
* Templates used for PageTable need a file associated (otherwise nothing gets rendered)
* This render method is meant for sites where the PageTable templates only render part of the layout, not complete websites. But you also can define what will be rendered (see below).

## Options

### Render Layout instead of table rows

Check this for seeing the rows rendered. You can easily turn off the complete functionality by unchecking this.

### Path to Stylesheet

Since the parts are unstyled by default, it is a good idea to define styles for them. All rendered templates are encapsulated in a div with the class "renderedLayout" so you can style them with:

´´´CSS
div.renderedLayout h2{
  color: green;
}
´´´

The path is to be set relative to your templates' folder.

### Reset Admin CSS

Since the parts are rendered inside the Admin, common styles of the Admin Interface apply also to your layout parts. This is not a bad thing, because especially text styles are well integrated in your admin's theme. But if you like to override the admin styles in your table rows completely (more or less), just check this box. Don't forget to define a custom CSS then!

## Advanced

Since this module is meant for parts of your layout you already have defined for your frontend templates, it is a good idea to use a preprocessor like Stylus, Sass or Less for building the custom CSS file. Just outsource your layout part definitions in an extra file, compile that in a separete CSS file and use this as custom CSS for this module. Since your CSS should be built in a modular way, this works pretty well ;-) Will write a tutorial with a use case once finished testing.



