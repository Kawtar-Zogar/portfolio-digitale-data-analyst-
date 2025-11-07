# 🌟 Data Mart Vente et Business Intelligence (DM Vente Project)

## Solution BI Intégrale : Modélisation, ETL et Analyse des Ventes

Ce dépôt présente une solution complète d'Intelligence d'Affaires (BI) centrée sur l'analyse des ventes. Le projet démontre le cycle de vie complet du Data Warehousing, de la modélisation à l'analyse, en utilisant **SQL Server Integration Services (SSIS)** et **Power BI**. Ce projet montre comment les données brutes sont transformées en aperçus exploitables pour la prise de décision.

---
**[Photo de couverture du Dashboard Ventes]**
![Aperçu du Tableau de Bord Principal](./Ressources/Dashboard_Final.png) 
---

### Aperçu Détaillé du Projet (Project Overview)

L'objectif الرئيسي كان تصميم، تطبيق ونشر Data Mart بالاعتماد على **Schéma en Étoile** لتحليل أداء المبيعات، تجزئة العملاء وفعالية المنتجات. تم بناء خطوط أنابيب ETL لسحب، تنظيف وإعادة صياغة البيانات في Data Mart منظم.

### Outils et Technologies Clés Utilisés:

* **SQL Server:** لإدارة قواعد البيانات واستضافة الـ Data Mart Vente.
* **SSIS (SQL Server Integration Services):** لأتمتة عمليات ETL، إدارة مفاتيح البدائل (Lookups) وتطبيق التحويلات.
* **Schéma en Étoile:** النموذج البعدي المعتمد في Data Warehouse.
* **Power BI:** لإنشاء لوحة تحكم تفاعلية توفر تحليلات المبيعات، العملاء والمنتجات.

---

## 1. Modélisation et Conception du Data Mart (Design)

Le Data Mart a été développé selon une architecture **Schéma en Étoile** لتسهيل الاستعلامات والتحليل.

![Schéma en Étoile du DM Vente](./Ressources/Schema_Etoile.png)

---

## 2. Processus ETL Détaillé (Extraction, Transformation, Chargement)

Le pipeline ETL géré par SSIS يضمن جودة وتسلسل عمليات التحميل.

### A. Flux de Contrôle (Control Flow)

Le Flux de Contrôle ينظم ترتيب التنفيذ، ويضمن تحميل جداول الأبعاد قبل جدول الوقائع:

![Flux de Contrôle SSIS - Séquence ETL](./Ressources/Control_Flow.png)

### B. Transformations et Chargement (4 Data Flows Essentiels)

العملية تتضمن تحويلات محددة لضمان النظافة والتكامل:

* **1. Chargement Dimension Date & Client:**
    ![Data Flow DimDate](./Ressources/Data_Flow_01_DimDate.png)
* **2. Chargement Dimension Produit:**
    ![Data Flow DimClient](./Ressources/Data_Flow_02_DimClient.png)
* **3. Chargement Table des Faits (FactSales):**
    ![Data Flow FactProduct](./Ressources/Data_Flow_03_DimProduct.png)
* **4. Chargement Final Fact Table (Lookups):**
    ![Data Flow FactTable](./Ressources/Data_Flow_04_FactTable.png)

---

## 3. Reporting et Analyse des Résultats (Power BI)

Le Tableau de Bord Power BI يقدم واجهة ديناميكية لاستكشاف البيانات.

![Détails de l'Analyse des Ventes sur Power BI](./Ressources/Dashboard_Detail.png)
