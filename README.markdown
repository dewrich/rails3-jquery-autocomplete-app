# rails3-jquery-autocomplete Example Application

This app is meant to provide more clarity on how to use the rails3-jquery-autocomplete gem.

# The Application, step by step

## Create the app

Use the rails command to create a new application

    rails new rails3-jquery-autocomplete -J
    
The _-J_ option is used to skip prototype, at this point I assume you won't need it.

## Gem requirements

The first thing to do is, add the following line to the Gemfile:

    gem 'rails3-jquery-autocomplete'
    gem 'nifty-generators'

This will include the rails3-jquery-autocomplete and Ryan Bates' nifty-generators gem as dependencies for the application.

We will use nifty-generators to speed things up a bit.

Now, make sure you install the required gems by running:

    bundle install
    
## Javascript files

Go to [http://jqueryui.com/download](http://jqueryui.com/download) and create a custom build for jQuery-UI. Obviously, make sure you select the Autocomplete widget.

Click on download and extract all the files in the zip file you just downloaded.

Copy the files on the *js* folder to the *public/javascripts* folder on your app.

Copy the files on the *css* folder to the *public/stylesheets* folder on your app.

Go to [http://github.com/rails/jquery-ujs](http://github.com/rails/jquery-ujs) and copy *rails.js* to the *public/javascripts* folder on your app.

## Include the files on your layout

Open app/views/layouts/application.html.erb and put the following lines on the <head> section:

    <head>
      <%= javascript_include_tag 'rails.js', 'jquery-1.4.2.js', 'jquery-ui-1.8.2.custom.min.js' %>
      <%= stylesheet_link_tag 'jquery-ui-1.8.2.custom.css' %>
    </head>

## Models

