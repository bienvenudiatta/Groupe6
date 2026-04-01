# 🔐 Projet : Infrastructure Sécurisée avec Hyper-V, Active Directory, IIS, SMTP et pfSense

## 📌 Description

Ce projet consiste à mettre en place une infrastructure réseau virtualisée sécurisée utilisant **Hyper-V** et **pfSense**, avec plusieurs serveurs Windows répartis entre un réseau interne (LAN) et une zone démilitarisée (DMZ).

---

## 🎯 Objectifs

* Virtualiser des serveurs avec Hyper-V
* Mettre en place un **Active Directory (AD)**
* Héberger une application web avec **IIS**
* Configurer un service **SMTP**
* Sécuriser le réseau avec **pfSense (Firewall)**
* Mettre en place une **DMZ (zone exposée)**

---

## 🖥️ Architecture du projet

### 🔹 Machines virtuelles

| Nom     | Rôle                   | Réseau          | IP                |
| ------- | ---------------------- | --------------- | ------------      |
| DC1     | Active Directory + DNS | LAN             | 192.168.100.10/24 |
| WEB1    | Serveur Web (IIS)      | DMZ             | 10.10.10.10/24    |
| MAIL1   | Serveur SMTP           | DMZ             | 192.168.2.20/24   |
| PFSENSE | Firewall / Routeur     | WAN / LAN / DMZ | -                 |

---

## 🌐 Réseau

* **WAN (Réseau Externe)** → Internet
* **LAN (Réseau Interne)** → réseau sécurisé (AD)
* **DMZ (zone exposée)** → services accessibles depuis Internet

👉 **pfSense** assure :

* Routage entre réseaux
* Filtrage (firewall)
* NAT (accès Internet)

---

## ⚙️ Technologies utilisées

* Hyper-V
* Windows Server 2022
* Active Directory
* DNS
* IIS (Internet Information Services)
* SMTP Server
* pfSense

---

## 🚀 Étapes de réalisation

### 1️⃣ Virtualisation

* Création des machines virtuelles sous Hyper-V
* Installation de Windows Server et pfSense

---

### 2️⃣ Configuration réseau

* Création de 3 switches :

  * WAN (Externe)
  * LAN (Interne)
  * DMZ (Interne ou privé)
* Configuration des interfaces pfSense :

  * WAN → Internet
  * LAN → 192.168.100.1/24
  * DMZ → 10.10.10.1/24

---

### 3️⃣ Configuration Active Directory

* Installation du rôle AD DS
* Création du domaine (ex: `monprojet.local`)
* Gestion des utilisateurs

---

### 4️⃣ Configuration IIS

* Installation du serveur Web
* Déploiement d’une application web
* Test d’accès depuis le client

---

### 5️⃣ Configuration SMTP

* Installation et configuration du service mail
* Test d’envoi de messages

---

### 6️⃣ Sécurité avec pfSense

* Création de règles firewall :

  * Autoriser WAN → DMZ (HTTP, SMTP)
  * Bloquer WAN → LAN ❌
  * Autoriser LAN → Internet ✔️
* Configuration NAT

---

### 7️⃣ Test client

* Utilisation du PC physique comme client
* Accès aux services :

  * Web (IIS via DMZ)
  * Mail (SMTP)
  * Domaine (AD via LAN)

---

## 📸 Captures d’écran

*(Ajouter ici les images du projet)*

---

## 📂 Structure du projet

```
/docs
/screenshots
/scripts
```

---

## 💡 Résultats

* Infrastructure sécurisée avec séparation LAN / DMZ
* Accès contrôlé aux services
* Protection du serveur Active Directory

---

## 🔥 Auteur

* Nom : Ibrahima DIALLO
* Nom : Bienvenu DIATTA
* Nom : Bassirou DIAO
* Projet académique – Systèmes, Réseaux

---

## 📌 Remarque

Les fichiers ISO et machines virtuelles ne sont pas inclus pour des raisons de taille et de licence.

---
