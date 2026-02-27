# Ansible_roles_users_nginxserver

Configuration des machines virtuelles à l’aide d’ansible : création d'utilisateur et mise en place du serveur web nginx.

**L'infrastruture Cloud préalablement déployée via Terraform**

**1. Cloud public Microsoft Azure et Cloud privé Openstack**

    Description de l'infrastructure cloud : 
    
      - trois machines virtuelles : une dans un sous réseau Vnet1
        et les deux autres (qui sont les machines à configurer à l'aide d'Ansible) dans un réseau privé Vnet2.
      
      - La machine du sous réseau Vnet1 est accéssible depuis l'extérieur en ssh. 
      
      - Les machines du réseau Vnet2 sont uniquement accéssibles en ssh depuis la machine du réseau Vnet1.
      
      - Les machines du réseau Vnet2 sont administrées depuis la machine du réseau Vnet1 où est installée Ansible. 
       
  **Repository vers l'infrastructure Cloud déployée via Terraform :**  
  
      - Cloud publique Microsoft Azure : https://github.com/Loic-Feukam/IaC_Azure_Terraform-
      
      - Cloud privé OpenStack : https://github.com/Loic-Feukam/IaC_Openstack_Terraform-

 
 **2. Configura tion des machines avec Ansible**

Rôle Ansible personnalisé développé afin d’automatiser les tâches suivantes : 

 1️⃣ Création d’un utilisateur 

 2️⃣ Génération d’une paire de clés SSH

   - Authentification sécurisée sans mot de passe.

   - Accès direct à la session de l’utilisateur x.

 3️⃣ Installation et configuration du serveur web Nginx

 
