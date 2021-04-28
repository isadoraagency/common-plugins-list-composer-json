# common-plugins-list

This document contains all commonly used plugins list and instuctions
on how to work with WP-CLI (https://wp-cli.org/).
Please feel free to update the plugins list under this repository
in the plugins.txt with the ones you need.

In order to do a bunk installation of the plugins and activate them 
you have to first login via ssh to the VEGA. Once you logged in 
navigate to the site folder by typing cd sitename.etlspace.com

To install all common plugins via WP-CLI run the following command:
# wp plugin install (place here plugins.txt file content without parenthesis)

To install some speciefic plugin and activate it via WP-CLI run the following command:
# wp plugin install plugin-name --activate

all available plugins to install listed here https://plugins.svn.wordpress.org/

please note that you can find the plugin name under it's official
wordpress plugin page like here https://wordpress.org/plugins/autoptimize/
it will be "autoptimize"

To activate previously installed common plugins via WP-CLI run the following command:
# wp plugin activate --all

To deativate previously installed common plugins via WP-CLI run the following command:
# wp plugin deactivate --all

Advanced Custom Fields PRO should be uploaded and installed manually.

Issues you may experienced during plugins activation:
1. "Uploads folder /var/www/virtual/sitename.etlspace.com/wp-content/uploads/wpallimport/logs must be writable"
  In order to fix that please run the following commands:
    mkdir wp-content/uploads/wpallimport
    mkdir wp-content/uploads/wpallimport/logs
    chmod 777 wp-content/uploads/wpallimport
    chmod 777 wp-content/uploads/wpallimport/logs

If you met any other issue please update this document with the solution or contact me
by maksym@isadoradigitalagency.com   
