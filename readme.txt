=== Truckcoin WooCommerce Extension ===
Contributors: serhack, goldenhill
Tags: truckcoin, woocommerce, integration, payment, merchant, cryptocurrency, accept truckcoin, truckcoin woocommerce
Requires at least: 4.0
Tested up to: 4.8
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
 
Truckcoin WooCommerce Extension is a Wordpress plugin that allows to accept bitcoins at WooCommerce-powered online stores.

== Description ==

An extension to WooCommerce for accepting Truckcoin as payment in your store.

= Benefits =

* Accept payment directly into your personal truckcoin wallet.
* Accept payment in truckcoin for physical and digital downloadable products.
* Add truckcoin payments option to your existing online store with alternative main currency.
* Flexible exchange rate calculations fully managed via administrative settings.
* Zero fees and no commissions for truckcoin payments processing from any third party.
* Automatic conversion to truckcoin via real time exchange rate feed and calculations.
* Ability to set exchange rate calculation multiplier to compensate for any possible losses due to bank conversions and funds transfer fees.

== Installation ==

1. Install "Truckcoin WooCommerce extension" WordPress plugin just like any other WordPress plugin.
2. Activate
3. Setup your truck-wallet-rpc with a view-only wallet
4. Add your truck-wallet-rpc host address and Truckcoin address in the settings panel
5. Click “Enable this payment gateway”
6. Enjoy it!

== Remove plugin ==

1. Deactivate plugin through the 'Plugins' menu in WordPress
2. Delete plugin through the 'Plugins' menu in WordPress

== Screenshots == 
1. Truckcoin Payment Box
2. Truckcoin Options

== Changelog ==

= 0.1 =
* First version ! Yay!

= 0.2 =
* Bug fixes

== Upgrade Notice ==

soon

== Frequently Asked Questions ==

* What is Truckcoin ?
Truckcoin is completely private, cryptographically secure, digital cash used across the globe. See https://truckcoin.com for more information

* What is a Truckcoin wallet?
A Truckcoin wallet is a piece of software that allows you to store your funds and interact with the Truckcoin network. You can get a Truckcoin wallet from https://truckcoin.com

* What is truck-wallet-rpc ?
The truck-wallet-rpc is an RPC server that will allow this plugin to communicate with the Truckcoin network. You can download it from https://truckcoin.com with the command-line tools.

* Why do I see `[ERROR] Failed to connect to truck-wallet-rpc at localhost port 28881
Syntax error: Invalid response data structure: Request id: 1 is different from Response id: ` ?
This is most likely because this plugin can not reach your truck-wallet-rpc. Make sure that you have supplied the correct host IP and port to the plugin in their fields. If your truck-wallet-rpc is on a different server than your wordpress site, make sure that the appropriate port is open with port forwarding enabled.
