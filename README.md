# MEANS #

![image](http://beta.sailsjs.org/images/bkgd_squid.png =600x)

MEANS is a boilerplate seed project that gives you a great foundation to start building real-time MongoDB + ExpressJS + AngularJS + SailsJS, single page applications.  It uses all the features available in the SailsJS framework and follows the same folder structure.

SailsJS was created by [Mike McNeil](https://twitter.com/mikermcneil) and has gracefully open sourced it.  You can view documentation at [http://beta.sailsjs.org](http://sailsjs.org)

We've created a sample **TODO** module. Go ahead and sign in with a couple different users in multiple browsers to see how it all works.

<br/>

# Getting Started #

## Prerequisites ##
Before you begin, you should make sure you have installed all these prerequisites on your development machine.

####Node.js & npm#####
Download & Install Node.js and the npm package manager, if you encounter any problems, you can also use this Github Gist to install Node.js.

######MongoDB####
Download & Install MongoDB, and make sure it's running on the default port (27017).

####Bower####
You're going to use the Bower Package Manager to manage your front-end packages, in order to install it make sure you've installed Node.js and npm, then install bower globally using npm:
	
	$ npm install -g bower

####Grunt####
You're going to use the Grunt Task Runner to automate your development process, in order to install it make sure you've installed Node.js and npm, then install grunt globally using npm:

	$ npm install -g grunt-cli
Note: Your user might not have the permissions to install package globally, so use a super user or sudo or run with admin provledges for windows command


Ensure you have **Sails v0.10** installed on your machine by executing the following commands:

    $ sudo npm install sails@beta -g
    

This will install the CLI globally.  Once you have the Sails CLI installed, proceed to execute the following:

    
    $ git clone https://github.com/SharePointOscar/MEANS.git
    $ cd into repo folder
    $ npm install
    $ cd assets
    $ bower install

This will install all client and server side packages needed.  Upon succesfully running the commands above, you are ready to lift your app!  At the root of the project run the following

    $ sails lift

View the app on your local machine at [http://localhost:1337](http://localhost:1337)  


#Folder Structure #

```

├── api 								-- server-side<br/>
│   ├── controllers<br/>
│   ├── models<br/>
│   ├── policies<br/>
│   ├── responses<br/>
│   └── services<br/>
├── assets							-- client-side<br/>
│   ├── bower_components<br/>
│   ├── fonts<br/>
│   ├── images<br/>
│   ├── src							-- AngularJS components<br/>
├   	|── app<br/>
		|-- common<br/>
		  |-- directives<br/>
		  ├── models<br/>
		  ├── services<br/>
│   └── styles<br/>
├── config							-- SailsJS Configuration<br/>
│  <br/>
 ├── node_modules<br/>
│  <br/>
├── tasks							    -- Grunt Tasks<br/>
│   ├── config<br/>
│   └── register<br/>
├── tests								 -- Testing Scripts<br/>
│   ├── e2e<br/>
		  |-- controllers<br/>
│   └── unit
		  |-- adapters<br/>
		  ├── controllers<br/>
		  ├── models<br/>  		
 		  ├── policies<br/>
		  ├── services<br/>							
   ├── views<br/>
│   ├── auth<br/>
│   ├── home<br/>
│   └── layouts<br/>

	
```

# Built-in Features #

## Authentication ##
The project uses the solid [PassportJS](http://passportjs.org) authentication module, which supports Local(username/password) and OAuth for Facebook, Twitter, Github etc.  Adding providers is as easy as modifying the config/passport.js and specifying your provider information.  

<br/>

## Branding ##
MEANS comes with [Bootswatch Themes](http://bootswatch.com/) created by [Thomas park](http://thomaspark.me/) to change the Theme, simply modify the *assets/styles/importer.less* file.  We also included [Font Awesome](http://fortawesome.github.io/Font-Awesome/)  

<br/>

## Asset Management ##
MEANS asset pipeline is streamlined, including additional AngularJS or other frameworks and libraries is as easy as modifying the file located at *tasks/pipeline.js*

<br/>

## Grunt ##
Grunt is included with various tasks including concat, minifying, less compiling and uglify, but it is not required.  For more detail, view tasks/README.md  

<br/>

## Support for Multiple Layouts ##
It is typical for a website that has membership to have different Layouts than the public section.  Because of this, we've demonstrated how you can use a public layout for non-members and a private layout for members.

<br/>

## Internationalization using i18n ##
SailsJS comes multi-language support, and so we've configured it and show this on the home page of the project.

<br/>

## Unit and e2e Testing (Client-side and Server-side) ##
We've integrated Grunt Tasks for MochaJS unit testing.  We've created two tests, a **server-side Controller Unit Test** and a **server-side Model Unit Test**, all successful.

#### MochaJS Unit Testing ####
Just use the following command for MochaJS Unit Testing

	$ grunt test:unit

The result of executing this command is shown below.  

![image](assets/images/screenshots/grunt_unit_testing.png =500x)


#### Protractor e2e Testing ####
Just use the following command for MochaJS Unit Testing

	$ grunt protractor

The result of executing this command is shown below. 

![image](assets/images/screenshots/protractor_e2e_tests.png)

<br/>

## Screenshots ##

![image](assets/images/screenshots/sailng-app.png)
