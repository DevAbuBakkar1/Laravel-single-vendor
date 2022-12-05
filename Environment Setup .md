# Laravel-single-vendor
![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)

### Step 01 : install Laravel :-
        
composer create-project laravel/laravel example-app

### Step 02 : Install Bootstrap Auth : 
The Bootstrap and Vue scaffolding provided by Laravel is located in the laravel/ui Composer package, which may be installed using Composer:

```
composer require laravel/ui

```
Once the laravel/ui package has been installed, you may install the frontend scaffolding using the ui Artisan command:

```
// Generate basic scaffolding...
php artisan ui bootstrap
php artisan ui vue
php artisan ui react

// Generate login / registration scaffolding...
php artisan ui bootstrap --auth
php artisan ui vue --auth
php artisan ui react --auth
```
Before compiling your CSS, install your project's frontend dependencies using the Node package manager (NPM):    
```
npm install
```
Once the dependencies have been installed using npm install, you can compile your SASS files to plain CSS using Vite. The npm run dev command will process the instructions in your vite.config.js file. Typically, your compiled CSS will be placed in the public/build/assets directory:
```
npm run dev
```
### Step 03 : Installing Laravel Yajra DataTables:-

Run the following command in your project to get the latest version of the package:

```
composer require yajra/laravel-datatables-oracle:"^10.0"
```
If you are using most of the DataTables plugins like Buttons & Html, you can alternatively use the all-in-one installer package.
```
composer require yajra/laravel-datatables:^9.0
```
#### Configuration : 
This step is optional if you are using Laravel 5.5+
Open the file config/app.php and then add following service provider.

```
'providers' => [
    // ...
    Yajra\DataTables\DataTablesServiceProvider::class,
],
```
After completing the step above, use the following command to publish configuration & assets:
```
php artisan vendor:publish --tag=datatables
```
### Step 04 : Install Image Intervention :-
The best way to install Intervention Image is quickly and easily with Composer.
To install the most recent version, run the following command.
```
composer require intervention/image
```
#### Configuration :
After you have installed Intervention Image, open your Laravel config file config/app.php and add the following lines.

In the $providers array add the service providers for this package.

```
Intervention\Image\ImageServiceProvider::class,
```
Add the facade of this package to the $aliases array.
```
'Image' => Intervention\Image\Facades\Image::class,
```
By default Intervention Image uses PHP's GD library extension to process all images. If you want to switch to Imagick, you can pull a configuration file into your application by running one of the following artisan command.

Publish configuration in Laravel
```
php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravelRecent"
```
