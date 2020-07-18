# TestSystem

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

#### Server
- Homestead [Documentation](https://laravel.com/docs/7.x/homestead)
- To add a site:
    - Edit Homestead.yaml file
    - Add host to hosts file
    - Run
    ```bash
    vagrant reload --provision
    ```
  
- Laravel  
    - [Documentation](https://laravel.com/docs/6.x)
    - Install  
    ```bash
    composer global require laravel/installer
    ```
  
- Midnight commander 
    - [Documentation](https://midnight-commander.org/wiki/doc)
    - Install 
    ```bash 
    sudo apt-get install mc
    ```
    - To start, run 
    ```bash
    sudo mc
    ```
  
- ENV database setup
    - Edit .env
    ```dotenv
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=testsystem
    DB_USERNAME=homestead
    DB_PASSWORD=secret
    ```
  
#### Development
- Laravel IDE Helper
    - [Documentation](https://github.com/barryvdh/laravel-ide-helper) 
    - Install
    ```bash
    composer require --dev barryvdh/laravel-ide-helper
    ```
    - Register in **config/app.php**
    ```php
    Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
    ```
    - Generating Docs
    ```bash
    php artisan clear-compiled
    php artisan ide-helper:generate
    ```
    - Publish **config file**
    ```bash
    php artisan vendor:publish --provider="Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider" --tag=config
    ```
  
- "VKOVIC" Laravel Commando
    - [Documentation](https://github.com/vkovic/laravel-commando)
    - Install
    ```bash
    composer require vkovic/laravel-commando
    ```

#### Application

- Node Modules
    - Install
    ```bash
    npm install     
    ```
    - Run initial development styles and scripts
    ```bash
    npm run dev
    ```
    - Watch changes to styles and scripts 
    ```bash
    npm run watch
    npm run watch-poll
    ```
  
- Laravel Auth
    - Install
    ```bash
    composer require laravel/ui --dev
    php artisan ui vue --auth
    npm install
    npm run dev
    php artisan migrate
    ```
  
- Laravel Permission
    - [Documentation](https://docs.spatie.be/laravel-permission/v3/introduction/)
    - Install
    ```bash
    composer require spatie/laravel-permission
    ```
    - Register in **config/app.php**
    ```php
    'providers' => [
        // ...
        Spatie\Permission\PermissionServiceProvider::class,
    ];
    ```
    - Publish **Migration**
    ```bash
    php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider" --tag="migrations"
    ```
    - **Migrate**
    ```bash
    php artisan migrate
    ```
    - Publish **config file**
    ```bash
    php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider" --tag="config"
    ```
    - Extend for **PHP Storm**
- Vue
    - [Documentation](https://vuejs.org/)
- Vuex
    - [Documentation](https://vuex.vuejs.org/)
- Vue Router
    - [Documentation](https://router.vuejs.org/)
- Admin LTE
    - To install, run:
    ```bash
        npm install admin-lte@^3.0 --save
     ```
  
## Dev route

### User Seeder
- **User** uses HasRoles
- Created RolesAndPermissionsSeeder
    - Has superadmin, admin and idealist
    - TODO:
        - Add permissions to roles
- Created UsersTAbleSeeder
    - Creates one static superadmin and one static admin
    - Using **UserFactory**, created 50 idealist users
- Called both seeders in **DatabaseSeeder** 

```
Give examples
```

### Blade Setup
- [ ] Grab initial template
- [ ] Extract into includes
- [ ] Setup Layout
- [ ] Extend Layout to pages
- [ ] Cleanup controllers and routes 

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

## Contributing

## Versioning


## Authors

* **Rastko Savic** - [RastkoSavic GitHub](https://github.com/RastkoSavic)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
