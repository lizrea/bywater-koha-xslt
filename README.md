# koha-xslt-from-github

Automate grabbing xslt files from GitHub to store and use locally

This script is meant to be used with the koha-foreach command. For each site it will look in github for a matching branch in the format v<major_version>.<minor_version>/<koha_instance_name>. If it does not it exist, it will do nothing. If it does exist, it will copy the xsl files from the repo to /var/lib/koha/<koha_instance_name> and update the xslt system preferences to point to the files.

This script only uses libraries already used by Koha, so no external dependencies are needed.

If you are not using ByWater's repos ( and you probably aren't ) you'll want to modify this script.

# Usage

update-xslt-from-github --confirm --verbose

Running without --confirm will run the script in test mode. Verbosity is forced in test mode.

Crontab example:
@hourly instancename-koha /path/to/koha-xslt-from-github/update-xslt-from-github --confirm
