# A Magento 2 Patch to fix SearchTmp Queries aka "search_tmp hanging queries"

### Tested on:
* 2.3.4
* 2.3.5

# Installation Instructions
Download the Zip file from Github repo and unzip it on your Magento root directory, then the following commands:
* php bin/magento module:enable AQELTech_SearchTmp --clear-static-content
* php bin/magento setup:upgrade && php bin/magento setup:di:compile
#### If your Magento instance in production mode, then run also the following command to deploy the static content:
* php bin/magento setup:static-content:deploy --jobs=3
* php bin/magento cache:clean && php bin/magento indexer:reindex

### I still need help?
* Please raise an issue on this repo and we shall help you as best as we can.
