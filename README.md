# Groupe6
# 🔐 Projet : Infrastructure Sécurisée avec Hyper-V, Active Directory, IIS, SMTP et pfSense

## 📌 Description

Ce projet consiste à mettre en place une infrastructure réseau virtualisée sécurisée utilisant **Hyper-V** et **pfSense**, avec plusieurs serveurs Windows pour gérer les utilisateurs, héberger une application web et configurer un service de messagerie.

---

## 🎯 Objectifs

* Virtualiser des serveurs avec Hyper-V
* Mettre en place un **Active Directory (AD)**
* Héberger une application web avec **IIS**
* Configurer un service **SMTP**
* Sécuriser le réseau avec **pfSense (Firewall)**
* Simuler une architecture réseau sécurisée

---

## 🖥️ Architecture du projet

### 🔹 Machines virtuelles

| Nom     | Rôle                   | IP           |
| ------- | ---------------------- | ------------ |
| DC1     | Active Directory + DNS | 192.168.1.10 |
| WEB1    | Serveur Web (IIS)      | 192.168.1.20 |
| MAIL1   | Serveur SMTP           | 192.168.1.30 |
| PFSENSE | Firewall / Routeur     | 192.168.1.1  |

---

## 🌐 Réseau

* **WAN (Réseau Externe)** → connecté à Internet
* **LAN (Réseau Interne)** → réseau des serveurs
* **pfSense** joue le rôle de routeur et firewall entre WAN et LAN

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

* Création de deux switches :

  * WAN (Externe)
  * LAN (Interne)
* Configuration des interfaces pfSense :

  * WAN → Internet
  * LAN → réseau interne

---

### 3️⃣ Configuration Active Directory

* Installation du rôle AD DS
* Création du domaine (ex: `monprojet.local`)
* Gestion des utilisateurs

---

### 4️⃣ Configuration IIS

* Installation du serveur Web
* Déploiement d’une application web

---

### 5️⃣ Configuration SMTP

* Installation et configuration du service mail
* Test d’envoi de messages

---

### 6️⃣ Sécurité avec pfSense

* Configuration du firewall
* Règles de filtrage réseau
* NAT (accès Internet pour les VM)

---

### 7️⃣ Test client

* Utilisation du PC physique comme client
* Accès aux services :

  * Web (IIS)
  * Mail (SMTP)
  * Domaine (AD)

---

## 📸 Captures d’écran

*(Ajouter ici les images du projet)*

---

## 📂 Structure du projet

```id="82ns9f"
/docs
/screenshots
/scripts
```

---

## 💡 Résultats

* Infrastructure sécurisée fonctionnelle
* Communication entre serveurs
* Accès contrôlé via firewall pfSense

---

## 🔥 Auteur

* Nom : Ibrahima DIATTA
* Nom : Bienvenu DIATTA
* Nom : BAssirou Diao
* Projet académique – Systèmes, Réseaux et Télécoms

---

## 📌 Remarque

Les fichiers ISO et machines virtuelles ne sont pas inclus pour des raisons de taille et de licence.

---
