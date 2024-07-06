

|| [prerequisites](#prerequisites) ||
[Deployment](#deployment) ||
[Authors](#authors) ||

# TERRAFORM-IMPORT

Terraform peut importer l'infrastructure existante. Cela vous permet de récupérer les ressources que vous avez créées par d'autres moyens et de les gérer sous Terraform.
La fonction `terraform import` permet d'intégrer des ressources existantes, créées en dehors de Terraform, dans votre infrastructure Terraform.
## Technologies

**Terraform :** `terraform import`

dans notre cas dans le **Cloud AWS** la ressources a importer est une instance `EC2` mais vous pouvez utiliser d'autres ressources.
## Features

- Importez des ressources cloud ou d'autres ressources déjà créées dans votre infrastructure Terraform.

- Gérez et provisionnez ces ressources de manière centralisée avec Terraform.

- Éliminez la nécessité de gérer séparément les ressources créées manuellement ou avec d'autres outils.
## Prerequisites


- **AWS EC2 :** Avoir une EC2 lancé qui va nous servir d'infrastructure a importer.

- **Terraform :** Avoir Terraform installé sur sa machine suivre le lien suivant : https://developer.hashicorp.com/terraform/install .

## Installation


\
In your command prompt download the repo with the commands:
```bash
  git clone https://github.com/AnselmeG300/terraform-import.git

  cd terraform-import
  
  code . 
```

    
## Deployment


1. Identifiez l'infrastructure à importer ; 

![alt text](<image/1. identification de la ressource à importer dark.png>)

2. Récupérez les configurations l’infrastructure ; 

![alt text](<image/2. recuperation des parametres de l'infra dark.png>)

3. Déclarez l'importation ; 

![alt text](<image/3. declaration de l'importation dark.png>)

4. Déclarez la ressource (Important : Définir tous les arguments nécessaires, sinon l'infrastructure sera mise à jour lors du apply) correspondante à l'infrastructure à importer dans notre cas EC2 ; 

![alt text](<image/4. declaration ressource dark.png>)

5. Taper la commande ```terraform plan``` :  si le plan contient à la fois « import » et « change », vérifiez la définition des arguments ;

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

