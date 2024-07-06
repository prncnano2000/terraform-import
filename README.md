

|| [Prerequisites](#prerequisites) ||
[Deployment](#deployment) ||
[Authors](#authors) ||

# TERRAFORM-IMPORT

Terraform can import existing infrastructure. This allows you to take resources you've created in other ways and manage them in Terraform.
The `terraform import` function allows you to integrate existing resources, created outside of Terraform, into your Terraform infrastructure.

## Technologies

**Terraform :** `terraform import`

in our case in the **AWS Cloud** the resource to import is an `EC2` instance but you can use other resources.

## Features

- Import cloud resources or other resources already created into your Terraform infrastructure.

- Manage and provision these resources centrally with Terraform.

- Eliminate the need to separately manage resources created manually or with other tools.


## Prerequisites


- **AWS EC2:** Have an EC2 launched which will serve as infrastructure for us to import.

- **Terraform:** Have Terraform installed on your machine, follow the following link: https://developer.hashicorp.com/terraform/install.

## Installation


In your command prompt download the repo with the commands:
```bash
  git clone https://github.com/AnselmeG300/terraform-import.git

  cd terraform-import
  
  code . 
```

    
## Deployment


1. Identify the infrastructure to import; 

![alt text](<image/1. identification de la ressource à importer dark.png>)

2. Retrieve the infrastructure configurations;

![alt text](<image/2. recuperation des parametres de l'infra dark.png>)

3. Declare the import;

![alt text](<image/3. declaration de l'importation dark.png>)

4. Declare the resource (Important: Define all the necessary arguments, otherwise the infrastructure will be updated during apply) corresponding to the infrastructure to import in our EC2 case;

![alt text](<image/4. declaration ressource dark.png>)

5. Type the command ```terraform plan```: if the plan contains both “import” and “change”, check the definition of the arguments;

![alt text](<image/5. terraform plan dark.png>)
![alt text](<image/5. info plan  dark.png>)

6. Taper la commande ```terraform apply --auto-approve``` 

![alt text](<image/6. terraform apply dark.png>) 
![alt text](<image/6. info apply dark.png>)


## Authors

- [@AnselmeG300](https://github.com/AnselmeG300/terraform-cloud.git)


## License

[MIT](https://choosealicense.com/licenses/mit/)


## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

