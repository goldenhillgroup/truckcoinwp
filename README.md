# TruckcoinWP
A WooCommerce extension for accepting [TRKC - Truckcoin] (https://truckcoin/)

## Dependencies
This plugin is rather simple but there are a few things that need to be set up beforehand.

* A web server! Ideally with the most recent versions of PHP and mysql

* A Truckcoin wallet. You can find the official wallet [here](https://truckcoin/)

* [WordPress](https://wordpress.org)
WordPress is the backend tool that is needed to use WooCommerce and this Truckcoin plugin

* [WooCommerce](https://woocommerce.com)
This Truckcoin plugin is an extension of WooCommerce, which works with WordPress

* [BCMath](http://php.net/manual/en/book.bc.php)
A PHP extension used for arbitrary precision maths

## Step 1: Activating the plugin
* Downloading: First of all, you will need to download the plugin. You can download the latest release as a .zip file from https://github.com/goldenhillgroup/truckcoinwp/releases If you wish, you can also download the latest source code from GitHub. This can be done with the command `git clone https://github.com/goldenhillgroup/truckcoinwp.git` or can be downloaded as a zip file from the GitHub web page.

* Unzip the file truckcoinwp_release.zip if you downloaded the zip from the releases page [here](https://github.com/goldenhillgroup/truckcoinwp/releases).

* Put the plugin in the correct directory: You will need to put the folder named `truckcoin` from this repo/unzipped release into the WordPress plugins directory. This can be found at `path/to/wordpress/folder/wp-content/plugins`

* Activate the plugin from the WordPress admin panel: Once you login to the admin panel in WordPress, click on "Installed Plugins" under "Plugins". Then simply click "Activate" where it says "Truckcoin - WooCommerce Gateway"

## Step 2 Option 1: Use your wallet address and viewkey

* Get your Truckcoin wallet address starting with 'W'
* Get your wallet secret viewkey from your wallet

A note on privacy: When you validate transactions with your private viewkey, your viewkey is sent to (but not stored on) explorer.truckcoin.io over HTTPS. This could potentially allow an attacker to see your incoming, but not outgoing, transactions if he were to get his hands on your viewkey. Even if this were to happen, your funds would still be safe and it would be impossible for somebody to steal your money. For maximum privacy use your own truck-wallet-rpc instance.

## Step 2 Option 2: Get a Truckcoin daemon to connect to

### Option 1: Running a full node yourself

To do this: start the Truckcoin daemon on your server and leave it running in the background. This can be accomplished by running `./truckd` inside your Truckcoin downloads folder. The first time that you start your node, the Truck daemon will download and sync the entire Truckcoin blockchain. This can take several hours and is best done on a machine with at least 4GB of ram, an SSD hard drive (with at least 40GB of free space), and a high speed internet connection.

### Option 2: Connecting to a remote node
The easiest way to find a remote node and use one of the nodes offered. It will automatically connect you to a random node.

### Setup your Truckcoin wallet-rpc

* Setup a Truckcoin wallet using the truck-wallet-cli tool. If you do not know how to do this you can learn about it at [Truckcoin Tech](https://truckcointech.blogspot.com)

* [Create a view-only wallet from that wallet for security.](https://truckcointech.blogspot.com)

* Start the Wallet RPC and leave it running in the background. This can be accomplished by running `./truck-wallet-rpc --rpc-bind-port 28881 --disable-rpc-login --log-level 2 --wallet-file /path/viewOnlyWalletFile` where "/path/viewOnlyWalletFile" is the wallet file for your view-only wallet. If you wish to use a remote node you can add the `--daemon-address` flag followed by the address of the node. `--daemon-address truckcoin.io:28881` for example.

## Step 4: Setup Truckcoin Gateway in WooCommerce

* Navigate to the "settings" panel in the WooCommerce widget in the WordPress admin panel.

* Click on "Checkout"

* Select "Truckcoin GateWay"

* Check the box labeled "Enable this payment gateway"

* Check either "Use ViewKey" or "Use truck-wallet-rpc"

If You chose to use viewkey:

* Enter your Truckcoin wallet address in the box labeled "Truckcoin Address". If you do not know your address, you can run the `address` command in your Truckcoin wallet

* Enter your secret viewkey in the box labeled "ViewKey"

If you chose to use truck-wallet-rpc:

* Enter your Truckcoin wallet address in the box labeled "Truckcoin Address". If you do not know your address, you can run the `address` command in your Truckcoin wallet

* Enter the IP address of your server in the box labeled "Truckcoin wallet RPC Host/IP"

* Enter the port number of the Wallet RPC in the box labeled "Truckcoin wallet RPC port" (will be `28881` if you used the above example).

Finally:

* Click on "Save changes"

## Donating to the Devs :)
TRKC Address : `XGygR6Y3yhBg7FMuvsLhLQfFbcDTyCmXRF6nKbUxRFHEhqZMcB7VKHEBduCfjoDa3uYxS1HzKkhs3J6vGr4kxrGL2WkrraNwM`
