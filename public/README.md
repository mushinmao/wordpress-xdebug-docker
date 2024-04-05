# Get started!

## Configure Docker containers

First you need to download WordPress.
This can be done from the official website https://uk.wordpress.org/download/.

Create a `public/` folder and unpack the contents of `wordpress/` folder in the archive here.

Then run the command `docker compose up -d`.

## Configure Xdebug (for PhpStorm)

Open PhpStorm and go to File → Settings (Preferences on Mac) → Languages & Frameworks → PHP → Debug.
Under the Xdebug section, ensure that the Debug port is set to 9003 and the "***Can accept external connections***" option is checked.

Add a PhpStorm Server: Navigate to PHP → Servers. Add a new server with the name WordPress and the host localhost. Set the port to 8080. 
Ensure the path mappings are set correctly – the absolute path on the server for the `public/` folder should be `/var/www/html`.

### Optional

Install the Xdebug helper extension:  Install the Xdebug helper extension for Google Chrome.
Once installed, click on the bug icon and set the IDE key to PHPSTORM.


# Done!