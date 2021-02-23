# Composer template for Tome documentation projects

This project is a great place to start for building brand new Tome projects.

There isn't much here now, but keep posted and let me know if anything doesn't
work!

# Requirements

- PHP 7+
- [Composer](https://getcomposer.org/)
- [Drush](https://github.com/drush-ops/drush-launcher#installation---phar)
- SQLite and the related PHP extensions

## Usage

To create a new Tome Documentation project, run:

(You need composer 1)
```bash
composer install
```

```bash
drush tome:install
```

To start a local webserver, run:

```bash
drush runserver --uri "example.local:8888"
```

Login Admin User, run:

```bash
drush uli --uri "example.local:8888"
```

When you're ready to build your static site, run:

```bash
drush tome:static
```

## Symlinks

When composer install or update is ran, the "modules" and "themes" directories,
as well as the "settings.php" file, is symlinked into the "web" directory.

This is done to improve DX, but only works on systems that support `bash`, and
symlinks. If you're running Windows you'll probably want to write a custom
script to replace `symlink.sh`, and use the `mklink` command. Pull requests are
welcome to make this functionality cross-platform by default.

## Further reading

This project is largely based on [drupal-composer/drupal-project], so it's
recommended that you consult their [README.md] for more information.

[drupal-composer/drupal-project]: https://github.com/drupal-composer/drupal-project
[README.md]: https://github.com/drupal-composer/drupal-project/blob/8.x/README.md
[drupal-tome/tome-docker]: https://github.com/drupal-tome/tome-docker