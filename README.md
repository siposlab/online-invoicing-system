# Online Invoicing System (OIS)

Easy and lean invoicing for small businesses, consultants and freelancers, created using [AppGini](https://bigprof.com/appgini/).

## Features

* Easily define your billable items, whether products or services.
* View customers activity and the full invoices history of each client.
* Check which customers ordered which items.
* Multiple customizable templates for invoices.
* Apply discounts and taxes.
* Show invoice total in digits and letters.
* Price history for items to keep log of price changes and apply the correct price to invoices based on their issue date.

This application was created using AppGini, and therefore it shares the features of any AppGini application as well, including:

* Responsive Bootstrap apps that work beautifully on any device.
* Support for multiple users and user groups, with easy-to-configure per-table permissions.
* Quick and advanced search.
* Export your data to CSV to work on them in Excel or other spreadsheets.
* Import already-existing data from CSV files through a powerful import wizard.

*Disclaimer: AppGini itself is not an open source application, but applications generated by AppGini can be distributed as open source with any license of choice.*

## Installation

This is a PHP/MySQL web application that you run from a browser. You can install it either locally on your own PC, or to a web/intranet server.

### 1. Installing to a PC

####System requirements

This application can be installed on Windows, Linux and MacOS. Before installing, you should have the following software set up and running:

* A webserver (Apache, IIS, nginx, ... etc)
* PHP 5.2 or higher.
* MySQL 3.x and above; or MariaDB 5.1 and above.

If you don't have the above software installed, we recommend installing
[Xampp latest version](http://www.apachefriends.org/).

####Installation steps

1. [Download the latest version as a zip file](https://github.com/bigprof-software/online-invoicing-system/archive/master.zip).

2. Extract the contents of the zip file into a folder inside your document root. (*[more info about how to find your 'document root'](http://www.karelia.com/sandvox/help/z/Document_Root.html)*).

3. In your web browser, go to: `http://localhost/app-folder/` (change `app-folder` above to the name of the folder inside your document root where you extracted the zip in step 2).

4. You should now see the setup wizard in your browser. Just follow the steps!

### 2. Installing to a web/intranet server

####System requirements

This application can be installed on both Windows and Linux servers. Before installing, make sure your server has the following software:

* PHP 5.2 or higher
* MySQL 3.x and above; or MariaDB 5.1 and above.
	
Make sure your has access to a MySQL/MariaDB database. You might need to set up one in your server control panel. Please refer to your server documentation or the technical support staff	for help on this if necessary.

If your server has cPanel installed, here is a [screencast explaining how to install your application using cPanel](https://bigprof.com/appgini/screencasts/how-to-upload-your-appgini-web-application-to-a-web-server-using-ftp-and-cpanel).

####Installation steps

1. [Download the latest version as a zip file](https://github.com/bigprof-software/online-invoicing-system/archive/master.zip).

2. Extract the contents of the zip file and upload them to a folder inside your server document root. (*[more info about how to find your 'document root'](http://www.karelia.com/sandvox/help/z/Document_Root.html)*).

3. In your web browser, visit `http://server.com/app-folder/` (change `server.com` above to the actual domain name or IP address of your server, and change `app-folder` to the name of the folder inside your document root where you uploaded the files in step 2).

4. You should now see the setup wizard in your browser. Just follow the steps!

## Customization

Since this application was created using AppGini, you can easily customize it by opening the included AXP project file in AppGini. Examples of possible customization you can do from there include:

* [Changing the application theme](https://bigprof.com/appgini/screencasts/how-to-easily-change-your-appgini-application-theme).
* Adding more fields to existing tables, or entirely new tables to fit your use cases.
* Changing the options/behavior of any table/field in your application.
* For more details, check [the AppGini tutorials](https://bigprof.com/appgini/screencasts/).

You can also perform more advanced customization, like adding reports, changing validation rules, adding business logic, ... etc. through hooks. Please refer to the [hooks documentation](https://bigprof.com/appgini/help/advanced-topics/hooks) for more details.

_**Contributions to this project are always welcome :)**_

## Changelog

###### Version 2.3, released on Oct 16, 2017

* First commit to Github :)
* Revised and enhanced README.
* Various source code conflicts resolved.

###### Version 2.2, released on May 08, 2017

* Generated using AppGini 5.62
* Implemented PHPMailer as the mail function for apps, with SMTP support configurable in admin settings.
* Included hooks/__global.php in admin area.
* Added new hook in __global.php, sendmail_handler() for intercepting mail sending operations.
* Fixed PHP 7.1 compatibility issue.
* Fixed preg_replace calls with /e modifier.
* Added validation checks to make sure undefined data formats are properly handled.
* Fixed XSS vulnerability in quick search responsibly reported by Netsparker.
* Added hooks/README.html.
* Fixed error with line breaks in emails sent from the admin area.
* Bug fix with sorting of formatted lookup fields.
* Bug fix for array_map warning when a record is selected in a table with a non-numeric PK.

###### Version 2.1

* Generated using AppGini 5.61
* Improved detail view loading performance by preloading lookup values.
* Bug fixed: Redirects don't work correctly if a non-standard port is used. 
* Configurable detail view template in DataList so that it can be set in hooks. 
* Fixed sorting behavior of lookup fields containing numeric data in table view. 
* Fixed a bug with anonymous users unable to directly access tables that they are allowed to view. 
* Fixed bug with error reporting behavior of unique fields.

###### Version 2.0

* Generated using AppGini 5.60
* Separate prices table to keep check of the price history.
* Adding different types of reports.
* Automatic calcuation of the invoice total with or w/o adding taxes and discount.
* Ability to print your invoice using your company template.