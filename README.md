![Frame 78 (6)](https://user-images.githubusercontent.com/2342458/194182219-586adce1-9fa5-456f-bc8b-79624adfa21e.png)
# Kinsta - Statamic Boilerplate

An example of how to set **Statamic** up to enable deployment on Kinsta App Hosting services.

---
Kinsta is a developer-centric cloud host / PaaS. We’re striving to make it easier for you to share your web projects with your users. Focus on coding and building, and we’ll take care of deployment and provide fast, scalable hosting. + 24/7 expert-only support.

- [Start your free trial](https://kinsta.com/signup/?product_type=app-db)
- [Application Hosting](https://kinsta.com/application-hosting)
- [Database Hosting](https://kinsta.com/database-hosting)

## Installation
**Statamic** is a flat-file CMS, which means all the data is stored in the git repository. Before pushing the code to **Kinsta Application Hosting**, you have to [install it locally](https://statamic.dev/installing) and create a super user account. After doing this, commit and push all the changes to the repository.

Remember that **Kinsta Application Hosting** works best for stateless applications, which means that it will be best to work on your content locally and use **Kinsta** just to serve the website to users.

## Dependency Management
**Statamic** is based on Laravel. This means that it's a regular PHP-based application, so during the deployment process Kinsta will automatically install dependencies defined in your `composer.json` file.

## Environment Variables
Note that **Statamic** requires few environment variables to be set:
- `APP_KEY` - you can get the `APP_KEY` either by running `php artisan key:generate` locally or use [this generator](https://generate-random.org/laravel-key-generator)
- `APP_KINSTA` - set it `true`.

## Required buildpacks
> **Warning**
> Your first deploy will fail in most cases because it won't have all the required **Buildbacks**. Remember to set them up after the first deployment.

In most cases we want our application to also build our CSS/JS files we need to add two Buildpacks:
- Node JS
- PHP

## Web Server Setup
When deploying an application Kinsta will automatically create a web process with `heroku-php-apache2 public/`. It can be later altered in the `Processes` tab in the UI.

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

More info on the [Statamic](https://statamic.com/) website.

## Watch How to Set Up a Statamic Application on Kinsta
[![Watch the video](https://img.youtube.com/vi/JAA95gNt8kk/maxresdefault.jpg)](https://www.youtube.com/watch?v=JAA95gNt8kk)
