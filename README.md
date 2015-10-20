# generator-base-backbone

[![Build Status](https://secure.travis-ci.org/zguillez/generator-base-angularjs.png?branch=master)](https://travis-ci.org/zguillez/generator-base-angularjs) [![Code Climate](https://codeclimate.com/github/zguillez/generator-base-angularjs/badges/gpa.svg)](https://codeclimate.com/github/zguillez/generator-base-angularjs)

> [Zguillez](https://zguillez.io) | Guillermo de la Iglesia

### Yeoman generator for AngularJS webapp development. With RequireJS, Bootstrap, Sass, and templating with Jade.

![](http://zguillez.github.io/img/angularjs.png)

# Getting Started

### Install Yeoman

	npm install -g yo

### Yeoman Generators

To install generator-base-angularjs from npm, run:

	npm install -g generator-base-angularjs

Finally, initiate the generator:

	yo base-angularjs

If you have error on install try to update dependences manually:

```bash
sudo npm update
```
```bash
bower update
```

## Requeriments

### [NodeJS](https://nodejs.org/)

For update npm

	sudo npm install npm -g

### [Bower](http://bower.io/)

	npm install -g bower

### [Sass](http://sass-lang.com/)

	sudo gem install sass
	
**Documentation:**

* [https://nodejs.org/](https://nodejs.org/)
* [http://bower.io/](http://bower.io/)
* [http://sass-lang.com/](http://sass-lang.com/)

# Usage

Develop code on folder **/src**

	/src
		/data
		/images
		/scripts
			/collections
			/views
		/styles
		/templates
		
### Compile code

Use grunt task to compile code and deploy webapp

	grunt serve
	
THis will launch server on port 9000

	http://localhost:9000/
	
Distribute code is compileded on forder **/dist**

	/dist
		/css
		/data
		/images
		/js
		/lib
		/templates
		
### Styling

Sass files (\*.sass, \*.scss) must be located on **/src/styles** folder root.

* Grunt task **sass.js** will process the files into CSS files to folder **/src/styles/css**.
* Grunt task **copy.js** will copy all CSS files into **/src/styles/css** to folder **/dist/css** for ditribution.
* You can also create and edit CSS files in **/src/styles/css**.

### Templating

The NodeJS template engine JADE is implemented. Jade files (\*.jade) must be located on **/templates** folder root.

* Grunt task **jade.js** will process the files into HTML files to folder **/templates/html**.
* Grunt task **copy.js** will copy all CSS files into **/templates/html** to folder **/dist/templates** for ditribution.
* You can also create and edit HTML templates files in **/templates/html**.


You can use combined Jade and Lodash for templating:

	//templates/index.jade
	
	header#header
	section(class='content')
	header
		img(class='logo', src='images/backbone.png')
	.buttons.row
		<% _.forEach(libs, function(lib) { %>
		<%=  '<a href="' + lib.url + '" target="_black" data-bypass="data-bypass" class="btn btn-default btn-sm">' + lib.name + '</a>'  %>
		<% }); %>
	footer#footer
	
**Documentation:**

* [http://jade-lang.com/](http://jade-lang.com/)

# Contributing and issues

Contributors are welcome, please fork and send pull requests! If you have any ideas on how to make this project better then please submit an issue or send me an [email](mailto:mail@zguillez.io).

# License

©2015 Zguillez.io

Original code licensed under [MIT](https://en.wikipedia.org/wiki/MIT_License) Open Source projects used within this project retain their original licenses.

# Changelog

### v1.0.0 (October 20, 2015) 
* Initial AngularJS skeleton

Features:

* Bootstrap
* Jquery
* Sass
* Jade templating
* JSHint code chech
* Grunt tasks



