# terraform-al.( Always latest :) )
### Insures that you have the latest terraform binary
It works on linux and MacOs
This little wrapper takes care of updating your terraform.
Also it supports version pinning.
If in CWD it finds file .terraform-version it will download and use the version specified in file
this can be usefull for temporary pinning the working terraform version.

If you are using terraform to create infrastructure on internap or other openstack providers
Just create file
```
cat  ~/.internap-credentials.cfg

OS_AUTH_URL=https://identity.api.cloud.iweb.com/v2.0
OS_USERNAME=api-234242424
OS_PASSWORD=sdfgsdgfsdgsdgsgsggsgsg
OS_TENANT_NAME=inap-324232
```
### Install
install dependencies curl jq unzip (coreutils is needed on MacOs to get gsort)

Remove terraform if it was already installed

download terraform bash script and put it in /usr/local/bin
```
wget https://raw.githubusercontent.com/vladislavPV/terraform-al/master/terraform
mv terraform /usr/local/bin/
chmod  a+x /usr/local/bin/terraform
```
### Run
```
$ terraform plan
```