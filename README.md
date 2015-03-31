OATSEA Sandpit
=======

A test Symfony project created on March 31, 2015, 3:15 am to test basic Symfony configuration and the ability to use composer to do uptdates and installation.

To install using composer create a **composer.json** in the installation directory with the following contents:
```
{
    "sandpit": "oatsea/sandpit",
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/OATSEA/sandpit.git"
        }
    ],
    "require": {
        "oatsea/sandpit": "dev-master"
    }
}
```
then navigate to the directory you want to install Sandpit into and (assuming Composer is installed) at the command prompt type the commmand:
```
    $ composer install
```
to update the installation at a latter date:
```
    $ composer update
```
**THE END!**
