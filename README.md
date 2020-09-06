Symfony5 Fundamentals: Services, Config & Environments

## Setup

To get it working, follow these steps:

**Download Composer dependencies**

Make sure you have [Composer installed](https://getcomposer.org/download/)
and then run:

```
composer install
```

You may alternatively need to run `php composer.phar install`, depending
on how you installed Composer.

**Start the Symfony web server**

You can use Nginx or Apache, but Symfony's local web server
works even better.

To install the Symfony local web server, follow
"Downloading the Symfony client" instructions found
here: https://symfony.com/download - you only need to do this
once on your system.

Then, to start the web server, open a terminal, move into the
project, and run:

```
symfony serve
```

(If this is your first time using this command, you may see an
error that you need to run `symfony server:ca:install` first).

Now check out the site at `https://localhost:8000`

Have fun!

**Optional: Webpack Encore Assets**

This app uses Webpack Encore for the CSS, JS and image files. But
to keep life simple, the final, built assets are already inside the
project. So... you don't need to do anything to get thing set up!

If you *do* want to build the Webpack Encore assets manually, you
totally can! Make sure you have [yarn](https://yarnpkg.com/lang/en/)
installed and then run:

```
yarn install
yarn encore dev --watch
```
## Commands
Show service configuration options:
` php bin/console config:dump KnpMarkdownBundle`

Full list of services in container: `php bin/console debug:container`

List of service instance (logger). For named autowiring: `php bin/console debug:autowiring log`

System info and env variables: ` php bin/console about`

Set local secret env variable: `php bin/console secret:set SENTRY_DSN

Set env variable for prod: ` php bin/console secret:set SENTRY_DSN --env=prod``

List all secret variables: `php bin/console secret:list`

Create a Symfony command: `php bin/console make:command`

View command description: `php bin/console app:random-spell --help`

Make a Twig Extension: `php bin/console make:twig-extension`