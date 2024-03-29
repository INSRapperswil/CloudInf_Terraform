# CloudInf_Terraform
Docker Swarm Cluster on Digital Ocean with Terraform

## Preparing
For one of the Bash scripts you have to install the following on your computer:
```
sudo apt install jq
```
### DigitalOcean
Before you can start with this lab you have to create a [DigitalOcean](https://m.do.co/c/2983f9d0dc6d) account. When you have created an account you have to generate an [API token](https://cloud.digitalocean.com/account/api/tokens) (make sure you enable read and write access). Please write down you API token because [DigitalOcean](https://m.do.co/c/2983f9d0dc6d) will not show you the token again.

### SSH Key
When you not already have a SSH key then you can create one with the following command:
```
ssh-keygen -b 4096 -t rsa -C cloudinf@digitalocean -f digitalocean-id-rsa
```
Once the keys are generated, use the following command to add the private key to your SSH Agent (only required if the SSH key has a passphrase set):
```
ssh-add digitalocean-id-rsa
```

### Clone
Clone this repository to your computer:
```
git clone https://github.com/HSRNetwork/CloudInf_Terraform.git
```

## Exercise
Create a new file named `terraform.tfvars` and add the following lines:
```
do_token="YOUR DIGITALOCEAN API TOKEN"
public_key_path="PATH TO YOUR PUBLIC KEY FILE"
```

Issue `terraform init` to initialize the provider plugins.

Now you can solve the **TODOS** in the `main.tf` file.

## Cleanup
To cleanup your DigitalOcean instrastructure, run `terraform destroy`.
