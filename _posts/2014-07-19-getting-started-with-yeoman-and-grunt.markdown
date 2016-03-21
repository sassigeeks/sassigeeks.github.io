---
layout: post
title:  "Apple is wrong about 4inch iPhone's."
date:   2016-03-21 22:55:49
categories: Apple Devices
banner_image: "/media/desk.jpg"
featured: true
comments: true
---

Today during what felt like the most rushed and pointless Apple Keynote I've ever had the misfortune to sit through Apple claimed that ther were over 30 million 4" iPhone's in use which is why the company felt the need to develop the iPhone SE 4". I'd argue that the people aren't really bothered about a .6" screen jump on the iPhone 6 and 6S and the real reason they are still using the smaller iPhone is because they either don't want to or can't afford to upgrade. I might be wrong, but I predict here and now that the iPhone SE will be a huge flop even more so than the iPhone 5C. 

<!--more-->

# iPhone SE, unappologetically pointless.

The Grunt ecosystem is huge and it's growing every day. With literally hundreds of plugins to choose from, you can use Grunt to automate just about anything with a minimum of effort. If someone hasn't already built what you need, authoring and publishing your own Grunt plugin to npm is a breeze.

{% include image_caption.html imageurl="/media/gruntjs-1.jpg" title="GruntJS" description="Grunt is built on Node.js, and it’s available as a package via the Node package manager (npm)." %}

## Installing the CLI

** If you're upgrading from Grunt 0.3, please see [Grunt 0.3 Notes](http://gruntjs.com/upgrading-from-0.3-to-0.4#grunt-0.3-notes) **

In order to get started, you'll want to install Grunt's command line interface (CLI) globally. You may need to use sudo (for OSX, *nix, BSD etc) or run your command shell as Administrator (for Windows) to do this.

{% highlight bash %}
	npm install -g grunt-cli
{% endhighlight %}
    
This will put the `grunt` command in your system path, allowing it to be run from any directory.

Note that installing `grunt-cli` does not install the Grunt task runner! The job of the Grunt CLI is simple: run the version of Grunt which has been installed next to a `Gruntfile`. This allows multiple versions of Grunt to be installed on the same machine simultaneously.

## How the CLI Works

Each time grunt is run, it looks for a locally installed Grunt using node's require() system. Because of this, you can run grunt from any subfolder in your project.

If a locally installed Grunt is found, the CLI loads the local installation of the Grunt library, applies the configuration from your Gruntfile, and executes any tasks you've requested for it to run.

To really understand what is happening, read the code. It's very short.

## Working with an existing Grunt project

Assuming that the Grunt CLI has been installed and that the project has already been configured with a package.json and a Gruntfile, it's very easy to start working with Grunt:

1. Change to the project's root directory.
2. Install project dependencies with npm install.
3. Run Grunt with grunt.

That's really all there is to it. Installed Grunt tasks can be listed by running grunt --help but it's usually a good idea to start with the project's documentation.

## The Gruntfile

The `Gruntfile.js` or `Gruntfile.coffee` file is a valid JavaScript or CoffeeScript file that belongs in the root directory of your project, next to the `package.json` file, and should be committed with your project source.

A `Gruntfile` is comprised of the following parts:

* The "wrapper" function
* Project and task configuration
* Loading Grunt plugins and tasks
* Custom tasks

### Example Gruntfile

In the following Gruntfile, project metadata is imported into the Grunt config from the project's package.json file and the grunt-contrib-uglify plugin's uglify task is configured to minify a source file and generate a banner comment dynamically using that metadata. When grunt is run on the command line, the uglify task will be run by default.

{% highlight javascript %}
module.exports = function(grunt) {

	grunt.initConfig({
		pkg: grunt.file.readJSON('package.json'),
		uglify: {
			options: {
				banner: '/*! <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> */\n'
			},
			build: {
				src: 'src/<%= pkg.name %>.js',
				dest: 'build/<%= pkg.name %>.min.js'
			}
		}
	});

};
{% endhighlight %}
    
Most Grunt tasks rely on configuration data defined in an object passed to the `grunt.initConfig` method.

In this example, `grunt.file.readJSON('package.json')` imports the JSON metadata stored in `package.json` into the grunt config. Because `<% %>` template strings may reference any config properties, configuration data like filepaths and file lists may be specified this way to reduce repetition.

You may store any arbitrary data inside of the configuration object, and as long as it doesn't conflict with properties your tasks require, it will be otherwise ignored. Also, because this is JavaScript, you're not limited to JSON; you may use any valid JS here. You can even programmatically generate the configuration if necessary.

Like most tasks, the `grunt-contrib-uglify` plugin's uglify task expects its configuration to be specified in a property of the same name. Here, the banner option is specified, along with a single uglify target named build that minifies a single source file to a single destination file.

***

This extract of text has been used as a demonstration of the Astro Ghost Theme. For more information on Grunt, see http://gruntjs.com.
