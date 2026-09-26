# AutoLoc — Plateforme de gestion de location de véhicules multi-agences

## Objectifs du projet

AutoLoc est une entreprise de location de véhicules disposant de plusieurs agences 
réparties dans différentes villes. Ce projet vise à numériser l'ensemble du processus 
métier : réservation, contractualisation, facturation, suivi de flotte et relances 
automatiques, à travers une application back-end Spring Boot exposant une API REST.

Le projet est développé progressivement au fil des ateliers du module ASI 
(Architecture des Systèmes d'Information), en appliquant une architecture en couches 
(Presentation, Service, Repository, Domain) et les bonnes pratiques Spring Boot / 
Spring Data JPA.

## Acteurs du système

| Rôle | Description | Droits principaux |
|------|-------------|--------------------|
| **Client** | Particulier ou professionnel souhaitant louer un véhicule | Consulter les véhicules disponibles, créer/annuler une réservation, consulter ses contrats |
| **Agent d'agence** | Employé en charge de la gestion opérationnelle d'une agence | Gérer les véhicules, valider une réservation, établir un contrat, enregistrer un paiement |
| **Responsable d'agence (Manager)** | Supervise une agence et son personnel | Droits Agent + gestion des employés, consultation des statistiques de l'agence |
| **Administrateur** | Administre la plateforme | Gestion des agences, des catégories de véhicules, statistiques globales, configuration |

## Modules fonctionnels

- **Gestion des agences & de la flotte** : CRUD des agences, des véhicules et de leurs catégories ; suivi de la disponibilité et du statut.
- **Gestion des clients** : inscription, mise à jour du profil, historique des réservations et des contrats.
- **Réservation** : recherche de véhicules disponibles par ville, catégorie et période ; création, modification et annulation de réservations.
- **Contractualisation & paiement** : génération d'un contrat à la validation d'une réservation, enregistrement des paiements.
- **Tarification** : calcul du tarif selon la catégorie du véhicule, la durée, la période et les équipements optionnels.
- **Tâches planifiées** : libération automatique des véhicules en fin de location, alertes de contrats arrivant à échéance.
- **Reporting & qualité** : statistiques d'occupation et de chiffre d'affaires par agence.

## Stack technique

- **Langage / Build** : Java 17+, Maven
- **Framework** : Spring Boot, Spring Data JPA, Spring MVC
- **Base de données** : MySQL (développement)
- **Productivité** : Lombok
- **Outillage** : Git/GitHub, Postman, IntelliJ IDEA