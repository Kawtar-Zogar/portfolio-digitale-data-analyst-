# 🌟 Data Mart Vente et Business Intelligence (DM Vente Project)

## Solution BI Intégrale : Modélisation, ETL et Analyse des Ventes

Ce dépôt présente une solution complète d'Intelligence d'Affaires (BI) centrée sur l'analyse des ventes. Le projet démontre le cycle de vie complet du Data Warehousing, de la modélisation à l'analyse, en utilisant **SQL Server Integration Services (SSIS)** et **Power BI**. Ce projet montre comment les données brutes sont transformées en aperçus exploitables pour la prise de décision.

---
**[Photo de couverture du Dashboard Ventes]**
![Aperçu du Tableau de Bord Principal](./Ressources/Dashboard_Final_1.png) 
---

### Aperçu Détaillé du Projet (Project Overview)

L'objectif principal كان تصميم، تطبيق ونشر Data Mart بالاعتماد على **Schéma en Étoile** لتحليل أداء المبيعات، تجزئة العملاء وفعالية المنتجات. Les pipelines ETL ont été mis en place pour extraire, nettoyer et charger les données dans le Data Mart structuré.

### Outils et Technologies Clés Utilisés:

* **SQL Server:** Pour la gestion des bases de données source et l'hébergement du Data Mart Vente.
* **SSIS (SQL Server Integration Services):** Pour l'automatisation des processus ETL, la gestion des clés de substitution (Lookups) et l'application des transformations.
* **Schéma en Étoile:** Le modèle dimensionnel adopté pour la Data Warehouse.
* **Power BI:** Pour construire un Dashboard interactif fournissant des analyses sur les ventes, les clients et les produits.

---

## 1. Modélisation et Conception du Data Mart (Design)

Le Data Mart a été développé selon une architecture **Schéma en Étoile** pour faciliter les requêtes et l'analyse.

![Schéma en Étoile du DM Vente](./Ressources/Schema_Etoile.png)

---

## 2. Processus ETL Détaillé (Extraction, Transformation, Chargement)

Le pipeline ETL est géré par des packages SSIS et se divise en plusieurs étapes pour garantir la qualité et la séquence des chargements.

### A. Flux de Contrôle (Control Flow)

Le Flux de Contrôle orchestre l'ordre d'exécution des tâches, assurant le chargement des dimensions avant la table des faits:

![Flux de Contrôle SSIS - Séquence ETL](./Ressources/Control_Flow.png)

### B. Transformations et Chargement (4 Data Flows Essentiels)

Le processus inclut des transformations spécifiques pour le nettoyage et l'intégration des clés:

* **1. Chargement Dimension Client:**
    ![Data Flow DimClient](./Ressources/Data_Flow_02_DimClient.png)
* **2. Chargement Dimension Produit:**
    ![Data Flow DimProduct](./Ressources/Data_Flow_03_DimProduct.png)
* **3. Chargement Dimension Salesperson:**
    ![Data Flow DimSalesperson](./Ressources/Data_Flow_04_DimSalesperson.png)
* **4. Chargement Final Table des Faits (FactSales):**
    ![Data Flow FactTable](./Ressources/Data_Flow_05_FactTable.png)

---

## 3. Reporting et Analyse des Résultats (Power BI)

Le Tableau de Bord Power BI fournit une interface dynamique لـ l'exploration des données.

![Détails de l'Analyse des Ventes sur Power BI](./Ressources/Dashboard_Final_2.png)
