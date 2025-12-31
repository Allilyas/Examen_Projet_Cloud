# ☁️ Infrastructure Cloud de Supervision Centralisée 

![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Zabbix](https://img.shields.io/badge/Zabbix-D60000?style=for-the-badge&logo=zabbix&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)

> **Auteur :** ALLOUKH Ilyas

##  Description du Projet

Ce projet vise la mise en œuvre d'une **infrastructure de supervision centralisée** hébergée sur le cloud **Amazon Web Services (AWS)**. L'objectif est de déployer une solution capable de monitorer en temps réel un parc informatique hybride composé de serveurs **Linux (Ubuntu)** et **Windows Server**.

La solution technique repose sur la conteneurisation du serveur **Zabbix** via **Docker**, garantissant portabilité, isolation et facilité de déploiement.


L'infrastructure est déployée dans un VPC AWS avec la topologie suivante :

- **Réseau :** VPC unique avec sous-réseau public et Security Groups stricts.
- **Serveur :** Instance EC2 `t3.medium` hébergeant la stack Docker (Zabbix Server + Web + DB).
- **Agents :** Instances EC2 (Linux `t3.medium` & Windows `t3.medium`) avec agents Zabbix configurés.


##  Guide de Démarrage Rapide

 Prérequis

* Un compte AWS actif.

* Une paire de clés SSH (.pem) pour l'accès aux instances.

* Docker et Git installés sur la machine serveur.


## 🌐 Accès à l'Interface

Une fois le déploiement terminé, l'interface Web Zabbix est accessible via l'IP publique de votre instance AWS :

- **URL :** `http://<VOTRE_IP_PUBLIQUE>:80`
- **Login par défaut :** `Admin`
- **Mot de passe :** `zabbix`




