## Pure Storage Terraform Demo

This project is for a demonstration of the Pure Storage Terraform Provider.
The compute module is faked and just outputs the information that would be needed for storage allocation.

The demo uses 2 variables: `purestorage_flasharray` and `purestorage_apitoken` to connect to and authenticate with the Pure Storage FlashArray.  

### Instructions
```
$ mkdir -p ~/.terraform.d/plugins
$ wget https://github.com/devans10/terraform-provider-purestorage/releases/download/v0.4.1/terraform-provider-purestorage.linux.tar.gz 
$ tar -xzf terraform-provider-purestorage.linux.tar.gz
$ mv linux/terraform-provider-purestorage ~/.terraform.d/plugins/
$ git clone https://github.com/devans10/puredemo.git
$ cd puredemo
```

Edit `terraform.tfvars` to add your array FQDN (or IP address) and api_token

```
$ terraform init
$ terraform plan
$ terraform apply
$ terraform destroy
```
