## Docker Hub

View Dockerfiles:

- [markoshust/magento-nginx (Docker Hub)](https://hub.docker.com/r/markoshust/magento-nginx/)
  - 1.13
      - [`latest`, `1.13`, `1.13-7`](https://github.com/markshust/docker-magento/tree/master/images/nginx/1.13)
      - [`1.13-6`](https://github.com/markshust/docker-magento/tree/20.1.1/images/nginx/1.13)
      - [`1.13-5`](https://github.com/markshust/docker-magento/tree/18.1.1/images/nginx/1.13)
      - [`1.13-4`](https://github.com/markshust/docker-magento/tree/18.0.1/images/nginx/1.13)
      - [`1.13-3`](https://github.com/markshust/docker-magento/tree/15.0.1/images/nginx/1.13)
      - [`1.13-2`](https://github.com/markshust/docker-magento/tree/12.0.0/images/nginx/1.13)
      - [`1.13-1`](https://github.com/markshust/docker-magento/tree/11.1.5/images/nginx/1.13)
      - [`1.13-0`](https://github.com/markshust/docker-magento/tree/11.0.0/images/nginx/1.13)
- [markoshust/magento-php (Docker Hub)](https://hub.docker.com/r/markoshust/magento-php/)
  - 7.3
      - [`latest`, `7.3-fpm`, `7.3-fpm-0`](https://github.com/markshust/docker-magento/tree/master/images/php/7.3)
  - 7.2
      - [`7.2-fpm`, `7.2-fpm-3`](https://github.com/markshust/docker-magento/tree/master/images/php/7.2)
      - [`7.2-fpm-2`](https://github.com/markshust/docker-magento/tree/23.2.1/images/php/7.2)
      - [`7.2-fpm-1`](https://github.com/markshust/docker-magento/tree/23.1.1/images/php/7.2)
      - [`7.2-fpm-0`](https://github.com/markshust/docker-magento/tree/23.0.0/images/php/7.2)
  - 7.1
      - [`7.1-fpm`, `7.1-fpm-12`](https://github.com/markshust/docker-magento/tree/master/images/php/7.1)
      - [`7.1-fpm-11`](https://github.com/markshust/docker-magento/tree/23.2.1/images/php/7.1)
      - [`7.1-fpm-10`](https://github.com/markshust/docker-magento/tree/23.1.1/images/php/7.1)
      - [`7.1-fpm-9`](https://github.com/markshust/docker-magento/tree/23.0.0/images/php/7.1)
      - [`7.1-fpm-8`](https://github.com/markshust/docker-magento/tree/17.0.1/images/php/7.1)
      - [`7.1-fpm-7`](https://github.com/markshust/docker-magento/tree/16.2.0/images/php/7.1)
      - [`7.1-fpm-6`](https://github.com/markshust/docker-magento/tree/16.0.0/images/php/7.1)
      - [`7.1-fpm-5`](https://github.com/markshust/docker-magento/tree/15.0.1/images/php/7.1)
      - [`7.1-fpm-4`](https://github.com/markshust/docker-magento/tree/15.0.0/images/php/7.1)
      - [`7.1-fpm-3`](https://github.com/markshust/docker-magento/tree/14.0.1/images/php/7.1)
      - [`7.1-fpm-2`](https://github.com/markshust/docker-magento/tree/13.0.0/images/php/7.1)
      - [`7.1-fpm-1`](https://github.com/markshust/docker-magento/tree/11.1.5/images/php/7.1)
      - [`7.1-fpm-0`](https://github.com/markshust/docker-magento/tree/11.0.0/images/php/7.1)
- [markoshust/magento-elasticsearch (Docker Hub)](https://hub.docker.com/r/markoshust/magento-elasticsearch/)
  - 6.5
      - [`latest`, `6.5`, `6.5.4-0`](https://github.com/markshust/docker-magento/tree/master/images/elasticsearch/6.5)

## Setup

### Automated Setup (New Project)

> macOS & Linux Only

```bash
curl -s https://raw.githubusercontent.com/topvalue/m2_docker/master/lib/onelinesetup?token=AB5MMZ3Z75GSQHLH5VL5UBK5VSIRG | bash -s -- topvalue.local 2.3.3
```

With Example Data
```bash
curl -s https://raw.githubusercontent.com/topvalue/m2_docker/master/lib/onelinesetup?token=AB5MMZ3Z75GSQHLH5VL5UBK5VSIRG | bash -s -- topvalue.local with-samples-2.3.3
```

## Custom CLI Commands

- `bin/bash`: Drop into the bash prompt of your Docker container. The `phpfpm` container should be mainly used to access the filesystem within Docker.
- `bin/cli`: Run any CLI command without going into the bash prompt. Ex. `bin/cli ls`
- `bin/clinotty`: Run any CLI command with no TTY. Ex. `bin/clinotty chmod u+x bin/magento`
- `bin/composer`: Run the composer binary. Ex. `bin/composer install`
- `bin/copyfromcontainer`: Copy folders or files from container to host. Ex. `bin/copyfromcontainer vendor`
- `bin/copytocontainer`: Copy folders or files from host to container. Ex. `bin/copytocontainer --all`
- `bin/dev-urn-catalog-generate`: Generate URN's for PHPStorm and remap paths to local host. Restart PHPStorm after running this command.
- `bin/devconsole`: Alias for `bin/n98-magerun2 dev:console`
- `bin/download`: Download & extract specific Magento version to the `src` directory. Ex. `bin/download 2.3.3`
- `bin/fixowns`: This will fix filesystem ownerships within the container.
- `bin/fixperms`: This will fix filesystem permissions within the container.
- `bin/grunt`: Run the grunt binary. Note that this runs the version from the node_modules directory for project version parity. Ex. `bin/grunt exec`
- `bin/magento`: Run the Magento CLI. Ex: `bin/magento cache:flush`
- `bin/n98-magerun2`: Access the n98 magerun CLI. Ex: `bin/n98-magerun2 dev:console`
- `bin/node`: Run the node binary. Ex. `bin/node --version`
- `bin/npm`: Run the npm binary. Ex. `bin/npm install`
- `bin/pwa-studio`: (BETA) Start the PWA Studio server. Note that Chrome will throw SSL cert errors and not allow you to view the site, but Firefox will.
- `bin/redis`: Run a command from the redis container. Ex `bin/redis redis-cli monitor`
- `bin/remove`: Remove all containers.
- `bin/removevolumes`: Remove all volumes.
- `bin/restart`: Stop and then start all containers.
- `bin/root`: Run any CLI command as root without going into the bash prompt. Ex `bin/root apt-get install nano`
- `bin/rootnotty`: Run any CLI command as root with no TTY. Ex `bin/rootnotty chown -R app:app /var/www/html`
- `bin/setup`: Run the Magento setup process to install Magento from the source code, with optional domain name. Defaults to `magento2.test`. Ex. `bin/setup magento2.test`
- `bin/setup-pwa-studio`: (BETA) Install PWA Studio (requires NodeJS and Yarn to be installed on the host machine). Pass in your base site domain, otherwise the default `master-7rqtwti-mfwmkrjfqvbjk.us-4.magentosite.cloud` will be used. Ex: `bin/setup-pwa-studio magento2.test`
- `bin/start`: Start all containers, good practice to use this instead of `docker-compose up -d`, as it may contain additional helpers.
- `bin/status`: Check the container status.
- `bin/stop`: Stop all containers.
- `bin/update`: Update your project to the most recent version of `docker-magento`.
- `bin/xdebug`: Disable or enable Xdebug. Accepts params `disable` (default) or `enable`. Ex. `bin/xdebug enable`

## Misc Info

### Database

The hostname of each service is the name of the service within the `docker-compose.yml` file. So for example, MySQL's hostname is `db` (not `localhost`) when accessing it from within a Docker container. Elasticsearch's hostname is `elasticsearch`.

Here's an example of how to connect to the MySQL cli tool of the Docker instance:

```
bin/cli mysql -h db -umagento -pmagento magento
```

You can use the `bin/clinotty` helper script to import a database. This example uses the root MySQL user, and looks for the `dbdump.sql` file in your local host directory:

```
bin/clinotty mysql -h db -u root -pmagento magento < dbdump.sql
```

### Composer Authentication

First setup Magento Marketplace authentication (details in the [DevDocs](http://devdocs.magento.com/guides/v2.0/install-gde/prereq/connect-auth.html)).

Copy `src/auth.json.sample` to `src/auth.json`. Then, update the username and password values with your Magento public and private keys, respectively. Finally, copy the file to the container by running `bin/copytocontainer auth.json`.

### Email / Mailhog

View emails sent locally through Mailhog by visiting [http://{yourdomain}:8025](http://{yourdomain}:8025)

### Redis

Redis is now the default cache and session storage engine, and is automatically configured & enabled when running `bin/setup` on new installs.

Use the following lines to enable Redis on existing installs:

**Enable for Cache:**

`bin/magento setup:config:set --cache-backend=redis --cache-backend-redis-server=redis --cache-backend-redis-db=0`

**Enable for Full Page Cache:**
`bin/magento setup:config:set --page-cache=redis --page-cache-redis-server=redis --page-cache-redis-db=1`

**Enable for Session:**

`bin/magento setup:config:set --session-save=redis --session-save-redis-host=redis --session-save-redis-log-level=4 --session-save-redis-db=2`

You may also monitor Redis by running: `bin/redis redis-cli monitor`

For more information about Redis usage with Magento, <a href="https://devdocs.magento.com/guides/v2.3/config-guide/redis/redis-session.html" target="_blank">see the DevDocs</a>.

### Xdebug & VS Code

Install and enable the PHP Debug extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug).

Otherwise, this project now automatically sets up Xdebug support with VS Code. If you wish to set this up manually, please see the [`.vscode/launch.json`](https://github.com/markshust/docker-magento/blame/master/compose/magento-2/.vscode/launch.json) file.

### Xdebug & PHPStorm

1.  First, install the [Chrome Xdebug helper](https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc). After installed, right click on the Chrome icon for it and go to Options. Under IDE Key, select PHPStorm from the list and click Save.

2.  Next, enable Xdebug in the PHP-FPM container by running: `bin/xdebug enable`, the restart the docker containers (CTRL+C then `bin/start`).

3.  Then, open `PHPStorm > Preferences > Languages & Frameworks > PHP` and configure:

    * `CLI Interpreter`
        * Create a new interpreter and specify `From Docker`, and name it `markoshust/magento-php:7-2-fpm`.
        * Choose `Docker`, then select the `markoshust/magento-php:7-2-fpm` image name, and set the `PHP Executable` to `php`.

    * `Path mappings`
        * Don't do anything here as the next `Docker container` step will automatically setup a path mapping from `/var/www/html` to `./src`.

    * `Docker container`
        * Remove any pre-existing volume bindings.
        * Ensure a volume binding has been setup for Container path of `/var/www/html` mapped to the Host path of `./src`.

4. Open `PHPStorm > Preferences > Languages & Frameworks > PHP > Debug` and set Debug Port to `9001`.

5. Open `PHPStorm > Preferences > Languages & Frameworks > PHP > DBGp Proxy` and set Port to `9001`.

6. Open `PHPStorm > Preferences > Languages & Frameworks > PHP > Servers` and create a new server:

    * Set Name and Host to your domain name (ex. `magento2.test`)
    * Keep port set to `80`
    * Check the Path Mappings box and map `src` to the absolute path of `/var/www/html`

7. Go to `Run > Edit Configurations` and create a new `PHP Remote Debug` configuration by clicking the plus sign and selecting it. Set the Name to your domain (ex. `magento2.test`). Check the `Filter debug connection by IDE key` checkbox, select the server you just setup, and under IDE Key enter `PHPSTORM`. This IDE Key should match the IDE Key set by the Chrome Xdebug Helper. Then click OK to finish setting up the remote debugger in PHPStorm.

8. Open up `src/pub/index.php`, and set a breakpoint near the end of the file. Go to `Run > Debug 'magento2.test'`, and open up a web browser. Ensure the Chrome Xdebug helper is enabled by clicking on it > Debug. Navigate to your Magento store URL, and Xdebug within PHPStorm should now trigger the debugger and pause at the toggled breakpoint.
