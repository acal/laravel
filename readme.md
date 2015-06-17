## Laravel PHP Framework

[![Build Status](https://travis-ci.org/laravel/framework.svg)](https://travis-ci.org/laravel/framework)
[![Total Downloads](https://poser.pugx.org/laravel/framework/d/total.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Stable Version](https://poser.pugx.org/laravel/framework/v/stable.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Unstable Version](https://poser.pugx.org/laravel/framework/v/unstable.svg)](https://packagist.org/packages/laravel/framework)
[![License](https://poser.pugx.org/laravel/framework/license.svg)](https://packagist.org/packages/laravel/framework)

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, queueing, and caching.

Laravel is accessible, yet powerful, providing powerful tools needed for large, robust applications. A superb inversion of control container, expressive migration system, and tightly integrated unit testing support give you the tools you need to build any application with which you are tasked.

## Official Documentation

Documentation for the framework can be found on the [Laravel website](http://laravel.com/docs).

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](http://laravel.com/docs/contributions).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.

### License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)


#AC set-up Laravel on C9 IDE via: https://docs.c9.io/v1.0/docs/laravel and http://laravel.com/docs/4.2/quick and http://tutsnare.com/how-to-install-laravel-on-ubuntu-lamp/
#At Commnad line:
$rm README.md php.ini hello-world.php
$sudo composer self-update
$composer create-project laravel/laravel ./laravel --prefer-dist
$shopt -s dotglob
$mv laravel/* ./
$rm -rf laravel
$mkdir -p .composer/vendor/bin
$sudo nano /etc/apache2/sites-enabled/001-cloud9.conf
#Then in nano text editor:
# Change this line
DocumentRoot /home/ubuntu/workspace

#To following
DocumentRoot /home/ubuntu/workspace/public

#Next db config:
$mysql-ctl cli 
#Note credentials for MySQL
>use c9;
>select @@hostname;
# Note acal-laravel-1603523
>exit
# Run apache2 and see if Laravel home page appears
$composer
# to check if working

# download installer
$sudo composer global require "laravel/installer=~1.1"
#setting up path
export PATH="~/.composer/vendor/bin:$PATH" 
# Create a new route:
# open app/Http/routes.php file
# Add to bottom of file:
#Route::get('users', function()
#{
#    return 'Users!';
#});

# Views in app/resources/views
#welcome.blade.php