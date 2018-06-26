# Composer Package
This is boilerplate for composer package.

## Do not forget to tag the package
```
git tag v1.0
git push --tags
```

## Useful command to brushup
#### Package URL
packagist.org

#### Initialise 
```
composer init
```
#### Searching package
```
composer search packagename@package version
```
#### Installing packages
```
composer require packagename
```
#### If we have only composer.json
```
composer install
```
#### Update all the packages including lock file.
```
composer update
```
#### Installing development package
```
composer require --dev packagename
```
#### Dumping autoload
```
composer dumpautoload
```
#### Removing package
```
composer remove packagename
```
#### Creating project
```
composer create-project packagename foldername
```
#### Sample Repo JSON
```
{
    "name": "udayshi/php_composer_hello-world",
    "description": "My first Composer project",
    "license": "MIT",
    "authors": [
        {
            "name": "Uday Shiwakoti",
            "email": "shiuday@gmail.com"
        }
    ],
    "minimum-stability": "dev",
    "require": {
        "php": "^7.0"
    },
    "autoload": {
            "psr-4": {
                "HelloWorld\\": "src/HelloWorld/"
            }
    }
}
```
#### Sample Client JSON
```
{
  "name": "uday.shiwakoti/ctest",
  "type": "project",
  "license": "MIT",
  "authors": [
    {
      "name": "Uday Shiwakoti",
      "email": "shiuday@gmail.com"
    }
  ],

  "repositories": [
    {
      "type": "composer",
      "url": "https://wpackagist.org"
    },
    {
      "type": "composer",
      "url": "https://github.com"
    }
  ],
  "require": {
    "udayshi/hello-world": "*"
  },
  "require-dev" : {},
  "scripts": {
    "post-install-cmd": [
      "bash ./scripts/symlinks.sh"
    ],
    "post-update-cmd": [
      "bash ./scripts/symlinks.sh"
    ]
  }
}

```