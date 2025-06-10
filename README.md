# 📊 Timesheet Web - Application de Suivi du Temps

## 🎯 Vue d'ensemble
**Timesheet Web** est une application web moderne et complète pour le suivi du temps de travail, spécialement adaptée aux réglementations suisses et aux jours fériés genevois. Cette solution offre une interface intuitive pour la gestion des heures, des congés et des heures supplémentaires.

## ✨ Fonctionnalités principales

### 📋 Gestion des informations personnelles
- **Données employé** : Nom, prénom, période de travail
- **Configuration flexible** : Année de travail, dates de début/fin personnalisables
- **Paramètres vacances** : Gestion des congés reportés et actuels
- **Heures standard** : Configuration des heures de travail quotidiennes

### 🗓️ Suivi temporel avancé
- **Calendrier mensuel** : 12 onglets pour chaque mois de l'année
- **Saisie détaillée** : Matin et après-midi avec périodes multiples (début/fin 1 & 2)
- **Calculs automatiques** : Totaux journaliers, hebdomadaires et mensuels
- **Gestion des absences** : 5 types (Vacances, Maladie, Accident, Formation, Spécial)

### 🎄 Conformité locale suisse
- **Jours fériés genevois** : Intégration automatique des fêtes locales
- **Calcul de Pâques** : Algorithme précis pour les dates variables
- **Weekends différenciés** : Distinction samedi/dimanche pour les bonus

### ⏰ Gestion des heures supplémentaires
- **Classification intelligente** : Séparation jours ouvrables/weekends/fériés
- **Bonus automatiques** : 
  - Dimanche et fériés : +50% 
  - Samedi : +25%
- **Reports mensuels** : Cumul automatique entre les mois
- **Compensation flexible** : Paiement, récupération partielle ou complète

### 📈 Rapports et statistiques
- **Tableau de bord** : Vue d'ensemble avec indicateurs clés
- **Rapport mensuel détaillé** : Répartition par type d'heures
- **Graphiques visuels** : Répartition annuelle des jours travaillés
- **Analyses d'absences** : Détail par catégorie avec totaux

### 💾 Sauvegarde et synchronisation
- **Auto-sauvegarde** : Stockage automatique local toutes les 5 minutes
- **Export/Import JSON** : Sauvegarde complète des données
- **Chargement automatique** : Détection du fichier le plus récent
- **Gestion fichiers** : Drag & drop, sélection manuelle

## 🎨 Interface utilisateur

### Design moderne
- **Interface responsive** : Adaptation mobile et desktop
- **Gradients attractifs** : Design contemporain avec effets visuels
- **Code couleur intuitif** :
  - 🟦 Jours ouvrables (blanc)
  - 🟦 Weekends (bleu clair)
  - 🟣 Jours fériés (violet clair)
  - 🟦 Vacances (bleu)
  - 🟥 Maladie (rouge)
  - 🟧 Accident (orange)
  - 🟣 Formation (violet)
  - 🟢 Spécial (vert)

### Navigation fluide
- **Onglets organisés** : 16 sections principales
- **Panel de statut** : Indicateurs de sauvegarde en temps réel
- **Bouton flottant** : Accès rapide à la sauvegarde
- **Raccourcis clavier** : Ctrl+S (sauvegarder), Ctrl+P (imprimer)

## 🔧 Fonctionnalités techniques

### Validation et assistance
- **Auto-complétion** : Format HH:MM automatique pour les heures
- **Calculs en temps réel** : Mise à jour instantanée des totaux
- **Validation logique** : Vérification de cohérence des données
- **Alertes visuelles** : Signalement des journées incomplètes

### Gestion des données
- **Structure JSON** : Format standardisé pour l'export/import
- **Persistance locale** : Stockage navigateur fiable
- **Horodatage** : Suivi des modifications avec timestamps
- **Récupération d'erreur** : Mécanismes de sauvegarde robustes

## 📊 Métriques et indicateurs

### Dashboard principal
- **Heures totales** : Cumul annuel toutes catégories
- **Jours travaillés** : Compteur avec demi-journées
- **Moyenne quotidienne** : Calcul automatique
- **Heures attendues** : Basé sur les jours ouvrables
- **Heures supplémentaires** : Écart positif/négatif
- **Solde vacances** : Congés restants en temps réel

### Rapports détaillés
- **Répartition mensuelle** : Heures par catégorie et report
- **Compensation tracking** : Suivi des modes de récupération
- **Analyse d'écarts** : Comparaison réalisé vs attendu
- **Statistiques visuelles** : Graphiques de répartition annuelle

## 🚀 Points forts techniques

### Performance
- **Calculs optimisés** : Algorithmes efficaces pour les totaux
- **Mise à jour incrémentale** : Recalcul sélectif des données modifiées
- **Chargement rapide** : Interface responsive et fluide

### Fiabilité
- **Auto-sauvegarde** : Protection contre la perte de données
- **Validation robuste** : Contrôles de cohérence multiples
- **Gestion d'erreurs** : Mécanismes de récupération intégrés

### Flexibilité
- **Configuration adaptable** : Paramètres utilisateur personnalisables
- **Format standard** : Compatibilité JSON pour intégrations
- **Évolutivité** : Architecture modulaire pour extensions futures

## 📅 Cas d'usage typiques

1. **Saisie quotidienne** : Enregistrement rapide des heures matin/après-midi
2. **Gestion congés** : Planification et suivi des absences
3. **Calcul paie** : Export des données pour traitement RH
4. **Reporting mensuel** : Génération automatique de rapports
5. **Audit annuel** : Vue d'ensemble statistique complète

## 🎯 Public cible
- **Employés** : Suivi personnel du temps de travail
- **Managers** : Contrôle des heures équipes
- **RH/Paie** : Données fiables pour traitement
- **Consultants** : Facturation client précise
- **PME suisses** : Conformité réglementaire locale

Cette application représente une solution complète et moderne pour la gestion du temps de travail, alliant facilité d'usage et fonctionnalités avancées dans le respect des spécificités suisses et genevoises.
