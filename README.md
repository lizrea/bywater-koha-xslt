# koha-xslt-from-github

Automate grabbing xslt files from GitHub to store and use locally

This script is meant to be used with the koha-foreach command. For each site it will look in github for a matching branch in the format v<major_version>.<minor_version>/<koha_instance_name>. If it does not it exist, it will do nothing. If it does exist, it will copy the xsl files from the repo to /var/lib/koha/<koha_instance_name> and update the xslt system preferences to point to the files.

This script only uses libraries already used by Koha, so no external dependencies are needed.
