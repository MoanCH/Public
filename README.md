# 📊 Guide d'utilisation - Timesheet Web

## Vue d'ensemble
Timesheet Web est une application moderne de suivi du temps de travail conçue spécialement pour les entreprises genevoises. Elle prend en compte les jours fériés suisses et genevois, calcule automatiquement les heures supplémentaires et gère les différents types d'absences.

## 🏠 Onglet Information

### Informations Personnelles
- **Nom/Prénom** : Vos coordonnées personnelles
- **Période de Travail** : Définissez l'année de travail et les dates de début/fin de période

### Gestion des Vacances
- **Vacances restants année précédente** : Report de vacances non utilisées
- **Vacances année courante** : Allocation annuelle de vacances
- **Heures de travail standard par jour** : Base de calcul (généralement 8h)

### Heures Supplémentaires Initiales
- **Heures suppl. jours ouvrables** : Report du mois précédent
- **Heures suppl. week-end et fériés** : Report des heures majorées

### Configuration des Bonus
- **Bonus Samedi** : Majoration pour le travail du samedi (défaut: 125%)
- **Bonus Dimanche** : Majoration pour le travail du dimanche (défaut: 150%)
- **Bonus Jours Fériés** : Majoration pour les jours fériés (défaut: 150%)
- **Bonus Heures de Nuit** : Majoration pour le travail de nuit (défaut: 100%)
- **Période de nuit** : Définition des heures considérées comme travail de nuit

## 📅 Onglets Mensuels (Janvier à Décembre)

### Saisie des Heures
Chaque jour dispose de 4 créneaux horaires :
- **Matin** : 2 créneaux (début/fin)
- **Après-midi** : 2 créneaux (début/fin)

### Format de Saisie
- **HH:MM** : Format standard (ex: 08:30)
- **Raccourcis** : 
  - `8` devient automatiquement `08:00`
  - `830` devient `08:30`
  - `8.5` devient `08:30`

### Types d'Absences
- **V** - Vacances (fond bleu)
- **M** - Maladie (fond rouge)
- **A** - Accident (fond orange)
- **F** - Formation (fond violet)
- **S** - Spécial (fond vert)

### Calculs Automatiques
- **Total Heures** : Calcul automatique par jour
- **Total incl. Bonus** : Heures avec majorations appliquées
- **Alertes** : Jours avec moins d'heures que le standard en rouge

### Récapitulatif Mensuel
Chaque mois affiche :
- **Heures jours ouvrables** avec reports et récupérations
- **Heures week-end/fériés** avec bonus calculés
- **Options de compensation** :
  - À payer
  - Récupération partielle (avec saisie du nombre d'heures)
  - Récupération complète

## 📈 Onglet Rapport

### Cartes de Résumé
- **Heures Totales** : Somme de toutes les heures travaillées
- **Jours Travaillés** : Nombre de jours effectifs
- **Moyenne/Jour** : Moyenne des heures par jour travaillé
- **Heures Attendues** : Basé sur les jours ouvrables et heures standard
- **Heures Sup.** : Différence entre heures travaillées et attendues
- **Vacances Restants** : Solde de vacances disponibles

### Tableau Détaillé Mensuel
Pour chaque mois :
- Répartition heures ouvrables vs week-end/fériés
- Reports des mois précédents
- Totaux cumulés
- Écarts par rapport aux heures attendues
- Type de compensation choisi

## 📊 Onglet Statistiques

### Graphique Annuel
Répartition visuelle des jours par catégorie :
- Jours travaillés
- Week-ends
- Jours fériés
- Vacances
- Maladie
- Accident
- Formation
- Spécial

### Détails des Absences
Compteurs précis pour chaque type d'absence.

## 🔄 Onglet Synchronisation

### Sauvegarde Locale
- **Auto-save** : Sauvegarde automatique toutes les 5 minutes
- **Sauvegarde manuelle** : Bouton de sauvegarde immédiate
- **localStorage** : Stockage dans le navigateur

### Import/Export
- **Télécharger Sauvegarde** : Export JSON avec horodatage
- **Charger Fichier** : Import depuis un fichier JSON
- **Glisser-Déposer** : Interface intuitive pour l'import

### Liaison de Fichier
- **Lier Fichier** : Connecte l'application à un fichier JSON spécifique
- **Sauvegarde Directe** : Écrit directement dans le fichier lié
- **Chargement Automatique** : Recherche et charge automatiquement le fichier JSON le plus récent du dossier `./Json/`

## 🎄 Jours Fériés Genevois 2025

L'application intègre automatiquement :
- Nouvel An (1er janvier)
- Vendredi-Saint (calculé selon Pâques)
- Lundi de Pâques
- Ascension
- Lundi de Pentecôte
- Fête nationale (1er août)
- Jeûne Genevois (premier jeudi après le premier dimanche de septembre)
- Noël (25 décembre)
- Restauration (31 décembre)

## 🔧 Fonctionnalités Avancées

### Travail de Nuit
- Configuration des heures de nuit personnalisable
- Calcul automatique des heures de nuit par segment de travail
- Application des majorations selon les taux configurés

### Compensation Intelligente
- **Report automatique** des heures supplémentaires d'un mois à l'autre
- **Récupération flexible** : paiement, récupération partielle ou complète
- **Calculs en cascade** : les choix de compensation affectent les mois suivants

### Raccourcis Clavier
- **Ctrl+S** : Sauvegarde rapide
- **Ctrl+P** : Impression du rapport

### Indicateurs Visuels
- **Panneau de statut** : Affichage en temps réel de l'état des sauvegardes
- **Légendes colorées** : Identification rapide des types de jours
- **Alertes visuelles** : Jours avec heures insuffisantes

## 💡 Conseils d'Utilisation

1. **Saisie quotidienne** : Entrez vos heures chaque jour pour éviter les oublis
2. **Vérification mensuelle** : Contrôlez le récapitulatif mensuel en fin de mois
3. **Sauvegardes régulières** : Téléchargez une copie de sauvegarde mensuellement
4. **Configuration initiale** : Définissez correctement les taux de bonus selon votre convention
5. **Heures de nuit** : Configurez les heures de nuit si applicable à votre poste

## 🔒 Sécurité et Confidentialité

- **Stockage local** : Toutes les données restent dans votre navigateur
- **Aucun envoi** : Aucune donnée n'est transmise sur internet
- **Sauvegardes personnelles** : Vous contrôlez vos propres fichiers de sauvegarde
- **Respect de la vie privée** : Application totalement autonome

## 🆘 Dépannage

### Problèmes Courants
- **Données perdues** : Vérifiez le dossier `./Json/` pour un chargement automatique
- **Calculs incorrects** : Vérifiez la configuration des heures standard et bonus
- **Problème de sauvegarde** : Videz le cache navigateur si nécessaire

### Support
Cette application est conçue pour être autonome et ne nécessite aucune connexion internet après le premier chargement.
