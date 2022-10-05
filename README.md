![Frame 78 (6)](https://user-images.githubusercontent.com/2342458/194182219-586adce1-9fa5-456f-bc8b-79624adfa21e.png)
# Kinsta - Statamic Boilerplate

An example of how to set **Statamic** up to enable deployment on Kinsta App Hosting services.

> Kinsta’s Application Hosting is a service to run your web apps and any databases side by side in a hassle-free environment, tailored for developer needs and ease of use. App Hosting is currently in an invite-only beta phase, sign up for a test account at [kinsta.com/application-hosting](https://kinsta.com/application-hosting/).

## Dependency Management
**Statamic** is based on Laravel. This means that it's a regular PHP-based application, so during the deployment process Kinsta will automatically install dependencies defined in your `composer.json` file.

## Required buildpacks
Because in most cases we want our application to also build our CSS/JS files we need to add two Biuldpacks:
- Node JS
- PHP

## Environment Variables
Note that **Statamic** requires few environment variables to be set:
- `APP_KEY`
- `APP_URL` - just copy and paste your Kinsta domain here with a proper protocol
- `ASSET_URL` - just copy and paste your Kinsta domain here with a proper protocol

## Web Server Setup
The default web process will be `heroku-php-apache2`. In this example we've created an `.htaccess` file that reroutes all requests to `public/index.php` for Laravel. If you'd like to change this command you can go to the Processes section in MyKinsta for your application. You could use:
* `heroku-php-apache2 /public`
* `php artisan serve --host 0.0.0.0 --port 8080`

## What is Statamic?
Statamic is a powerful, flat-file CMS built on Laravel.

### Key Features
- There’s no database until you need one.
- It’s a front-to-back CMS until you need to go headless.
- It’s dynamically powered by PHP & Laravel until you need to go static.
- It’s full-stack until you go JAMstack.
- Host it on any modern PHP server until you want to go serverless.
- Use the control panel unless you don’t feel like it. Code editors are great too.
- You can version control everything unless you don’t want to.

More info on the [statamic.com](https://statamic.com/) website.
