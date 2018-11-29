# Laravel 5.2 Scaffold Generator
[![Travis](https://img.shields.io/travis/laralib/l5scaffold.svg?style=flat-square)](https://github.com/laralib/l5scaffold)
[![Packagist](https://img.shields.io/packagist/dt/laralib/l5scaffold.svg?style=flat-square)](https://packagist.org/packages/laralib/l5scaffold)

Hi, this is a scaffold generator for Laravel 5.2. (Laravel scaffold for Laravel 5.1? change branch to laravel-5.1 )

## Usage

### Step 1: Install Through Composer

```
composer config repositories.l5scaffold vcs https://github.com/gabelab2bora/l5scaffold.git
composer require 'laralib/l5scaffold:dev-patch-laravel5.7' --dev
```

```
composer require 'laralib/
```

### Step 2: Add the Service Provider

Open `config/app.php` and, to your **providers** array at the bottom, add:

```
"Laralib\L5scaffold\GeneratorsServiceProvider"
```

### Step 3: Run Artisan!

You're all set. Run `php artisan` from the console, and you'll see the new commands `make:scaffold`.

## Examples


```
php artisan make:scaffold Tweet --schema="title:string:default('Tweet #1'), body:text"
```
This command will generate:

```
app/Tweet.php
app/Http/Controllers/TweetController.php
database/migrations/2015_04_23_234422_create_tweets_table.php
database/seeds/TweetTableSeeder.php
resources/views/layout.blade.php
resources/views/tweets/index.blade.php
resources/views/tweets/show.blade.php
resources/views/tweets/edit.blade.php
resources/views/tweets/create.blade.php
```
And don't forget to run:

```
php artisan migrate
```

## Validations
```
php artisan make:scaffold Tweet --schema="firstname:string" --validator="lastname:unique(tweets,id),firstname:required|unique(tweets)"
```

## Localization
Localization required two arguments, the first being the `--localization` one which is a key value pair the key being the string that you want to reference the Localized value string by. 
```
php artisan make:scaffold Tweet --schema="firstname:string" --localization="key:value" --lang="country_code"
```

### Other Examples (new)

Same as above with use of the prefix. It will create the prefix in redirects of controller and the links of views (v1.0.7):
```
php artisan make:scaffold Tweet --schema="title:string:default('Tweet #1'), body:text" --prefix="admin"
```
Create the empty scaffold views, controller, seed, migration and model (v1.0.6):
```
php artisan make:scaffold Tweet
```
Create the empty scaffold (with prefix) views, controller, seed, migration and model (v1.0.7):
```
php artisan make:scaffold Tweet --prefix="admin"
```

## Scaffold
![image](http://i62.tinypic.com/11maveb.png)
![image](http://i58.tinypic.com/eqchat.png)
![image](http://i62.tinypic.com/20h7k8n.png)

###Data type Date (on view)
![image](http://i65.tinypic.com/29wooxl.png) 

###Data type Boolean (on view)
![image](http://i65.tinypic.com/afehl5.jpg)

# Todo task list
1 - More fields type

2 - Default tests file

3 - sass and js with gulp

**Send us your ideas.** (send message to @fernandobritofl (Twitter))


<br/><br/>
##Collaborators
 [Fernando Brito](https://github.com/fernandobritofl "fernandobritofl")
 <br/>[Sylvio Tavares](https://github.com/sylviot "Sylviot")
 <br/>[Raphael Heitor](https://github.com/raphaelheitor "raphaelheitor")
 <br/>[Alfred Nutile](https://github.com/alnutile "alnutile")
 <br/>[Sazzad Hossain Khan](https://github.com/itsazzad "itsazzad")
 <br/>[Alexander Makhaev](https://github.com/mankms "mankms")
 <br/>[Adam Brown](https://github.com/DeftNerd "DeftNerd")
 <br/>[TJ Webb](https://github.com/webbtj "webbtj")
 <br/>[Tsaganos Tolis](https://github.com/Dev-Force "Dev-Force")
 <br/>[Ryan Gurnick](https://github.com/ryangurn "ryangurn")
