# 📋 Guide d'utilisation - Timesheet Web

## Vue d'ensemble
Timesheet Web est une application de suivi du temps de travail spécialement conçue pour les employés suisses, avec une gestion automatique des jours fériés genevois. L'application permet de saisir précisément les heures de travail avec des sessions multiples par demi-journée et gère automatiquement les absences et congés.

## 🏗️ Structure de l'application

### Interface à onglets
L'application est organisée en plusieurs sections accessibles via des onglets :
- **Information** : Configuration personnelle et paramètres
- **Janvier à Décembre** : 12 onglets mensuels pour la saisie des heures
- **Rapport** : Synthèse annuelle et statistiques
- **Statistiques** : Graphiques et répartition des jours
- **Synchronisation** : Gestion des sauvegardes et imports/exports

## 📝 Fonctionnalités principales

### 1. Onglet Information
**Configuration personnelle :**
- Nom et prénom de l'employé
- Année de travail (modifiable, régénère automatiquement les calendriers)
- Période de travail (date de début et fin)

**Gestion des vacances :**
- Vacances restantes de l'année précédente
- Allocation de vacances pour l'année courante
- Heures de travail standard par jour (défaut : 8h)

**Jours fériés :**
- Affichage automatique des jours fériés suisses et genevois
- Calcul automatique basé sur l'année sélectionnée
- Inclut : Nouvel An, Vendredi-Saint, Lundi de Pâques, Ascension, Lundi de Pentecôte, Fête nationale, Jeûne Genevois, Noël, Restauration

### 2. Onglets mensuels (Janvier à Décembre)

**Structure de saisie avancée :**
Chaque jour dispose de :
- **Matin** : 2 sessions de travail (Début 1, Fin 1, Début 2, Fin 2)
- **Après-midi** : 2 sessions de travail (Début 1, Fin 1, Début 2, Fin 2)
- **Calculs automatiques** : Total matin, total après-midi, total journée
- **Gestion des absences** : Sélecteurs pour matin et après-midi

**Types d'absences :**
- **V** : Vacances (fond bleu clair)
- **M** : Maladie (fond rouge clair)
- **A** : Accident (fond orange clair)
- **F** : Formation (fond violet clair)
- **S** : Spécial (fond vert clair)

**Codage couleur des jours :**
- Blanc : Jours ouvrables
- Bleu clair : Week-ends
- Violet clair : Jours fériés

**Fonctionnalités de saisie :**
- Auto-complétion des heures (saisie "8" devient "08:00")
- Formats acceptés : 8, 8:, 8.30, 8:30
- Validation automatique des heures
- Désactivation automatique des champs lors de sélection d'absence

### 3. Calculs automatiques

**Heures bonus week-end et jours fériés :**
- Dimanche et jours fériés : 150% (coefficient 1.5)
- Samedi : 125% (coefficient 1.25)
- Affichage dans la colonne "Total incl." pour distinction

**Totaux journaliers :**
- Calcul automatique matin + après-midi
- Alerte visuelle si heures inférieures au standard sur jour ouvrable
- Prise en compte des absences dans les calculs

### 4. Onglet Rapport

**Cartes de synthèse :**
- Heures totales travaillées
- Nombre de jours travaillés
- Moyenne d'heures par jour
- Heures attendues (jours ouvrés × heures standard)
- Heures supplémentaires (différence entre travaillé et attendu)
- Vacances restantes (avec code couleur selon le solde)

**Tableau mensuel détaillé :**
- Répartition par mois des heures matin/après-midi
- Jours ouvrés vs jours travaillés
- Écarts par rapport aux heures attendues
- Moyennes journalières
- Comptabilisation des absences
- Heures week-end et bonus séparés

### 5. Onglet Statistiques

**Graphique annuel :**
- Répartition visuelle des types de jours
- Barres colorées pour chaque catégorie
- Données numériques sur chaque barre

**Détails des absences :**
- Cartes individuelles par type d'absence
- Compteurs précis en demi-journées
- Visualisation claire de la répartition

### 6. Onglet Synchronisation

**Sauvegarde locale :**
- Auto-sauvegarde toutes les 5 minutes
- Sauvegarde immédiate après chaque modification
- Stockage dans le navigateur (localStorage)

**Import/Export :**
- Zone de glisser-déposer pour fichiers JSON
- Téléchargement de sauvegardes horodatées
- Convention de nommage : `timesheet_[Nom]_[Année].json`

**Nettoyage :**
- Effacement sélectif du cache
- Reset complet des données
- Confirmations de sécurité

## 🔧 Fonctionnalités techniques

### Chargement automatique
L'application recherche automatiquement au démarrage :
1. Données dans le localStorage du navigateur
2. Fichiers JSON dans le dossier `./Json/` avec conventions :
   - `timesheet_[année].json`
   - `timesheet_latest.json`
   - `timesheet.json`
   - `latest.json`
3. Sélection automatique du fichier le plus récent

### Panel de statut (coin supérieur droit)
- **localStorage** : Présence de données sauvées
- **Auto-save** : Statut de la sauvegarde automatique
- **Sync** : Statut de synchronisation
- **Dernière sauvegarde** : Horodatage de la dernière sauvegarde

### Raccourcis clavier
- `Ctrl + S` : Sauvegarde manuelle
- `Ctrl + P` : Impression du rapport
- `Ctrl + E` : Export CSV

### Bouton flottant
- Bouton "💾 Auto" en bas à droite
- Sauvegarde manuelle immédiate
- Feedback visuel lors de la sauvegarde

## 📊 Calculs et logique métier

### Jours ouvrables
- Lundi à vendredi, hors jours fériés
- Ajustement automatique selon les absences déclarées

### Heures attendues
- Jours ouvrables × heures standard par jour
- Exclusion automatique des jours d'absence

### Bonus week-end
- Calcul séparé des heures normales et avec bonus
- Distinction claire dans les rapports

### Vacances
- Suivi du solde : reports + allocation annuelle - consommé
- Alerte visuelle si solde négatif

## 🎨 Interface utilisateur

### Design moderne
- Gradient coloré et interface épurée
- Responsive design pour mobile et desktop
- Animations et transitions fluides

### Notifications
- Confirmations de sauvegarde
- Alertes d'erreur
- Messages de chargement automatique

### Légendes visuelles
- Codes couleur explicites sur chaque onglet mensuel
- Identification claire des types de jours et absences

## 🔄 Workflow recommandé

1. **Configuration initiale** : Remplir l'onglet Information
2. **Saisie quotidienne** : Entrer les heures dans les onglets mensuels
3. **Suivi régulier** : Consulter l'onglet Rapport pour le suivi
4. **Analyse** : Utiliser l'onglet Statistiques pour les tendances
5. **Sauvegarde** : Télécharger régulièrement via l'onglet Synchronisation

## 🛡️ Sécurité et fiabilité

- Sauvegarde automatique continue
- Validation des données saisies
- Confirmations pour les actions destructives
- Récupération automatique des données perdues
- Horodatage de toutes les sauvegardes

Cette application offre une solution complète et professionnelle pour le suivi du temps de travail, spécialement adaptée au contexte suisse et genevois.
