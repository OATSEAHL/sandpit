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

If you can't then run the website you probably need to fix the file security.  See Symfony for full details but probably do something like the following:

At the terminal prompt; navigate to the right directory (ie you can see the app folder) and do the following commands:

```
$ rm -rf app/cache/*
$ rm -rf app/logs/*

$ HTTPDUSER=`ps aux | grep -E '[a]pache|[h]ttpd|[_]www|[w]ww-data|[n]ginx' | grep -v root | head -1 | cut -d\  -f1`
$ sudo chmod +a "$HTTPDUSER allow delete,write,append,file_inherit,directory_inherit" app/cache app/logs
$ sudo chmod +a "`whoami` allow delete,write,append,file_inherit,directory_inherit" app/cache app/logs
```

**THE END!**
