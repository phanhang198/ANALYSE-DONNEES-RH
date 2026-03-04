On va appliquer le **Design Thinking** pour exploiter ce dataset et adresser un problème business.

# 🎯 Problématique cible

**Comment réduire l’attrition (Attrition = départ des employés) dans l’entreprise ?**

On va structurer cela avec les 5 étapes du **Design Thinking** :

---

# 1️⃣ Empathize (Comprendre les utilisateurs)

## 👤 Qui sont nos “utilisateurs” ?

* Employés
* Managers
* RH
* Direction

## 📊 Ce que le dataset nous dit

Variables importantes liées à l’attrition :

* `Age`
* `BusinessTravel`
* `DistanceFromHome`
* `JobSatisfaction`
* `EnvironmentSatisfaction`
* `WorkLifeBalance`
* `OverTime`
* `MonthlyIncome`
* `YearsAtCompany`
* `YearsSinceLastPromotion`
* `RelationshipSatisfaction`

## 🔍 Questions d’empathie

* Les employés qui quittent ont-ils un faible salaire ?
* Font-ils beaucoup d’heures supplémentaires (`OverTime`) ?
* Ont-ils peu évolué (`YearsSinceLastPromotion`) ?
* Ont-ils un mauvais équilibre vie pro/perso ?
* Sont-ils jeunes et mobiles ?

👉 Ici on commence par **analyse exploratoire (EDA)** pour comprendre les profils à risque.

---

🟡  OVERVIEW

<img width="900" height="493" alt="image" src="https://github.com/user-attachments/assets/55049f12-b822-4025-9996-7ca9b5d62167" />

🟡  DEFINE → Identifier les facteurs critiques
🎛️ Page 2 : Drivers d’Attrition
1️⃣ Attrition vs MonthlyIncome
👉 Voir si bas salaire = départ
<img width="752" height="509" alt="image" src="https://github.com/user-attachments/assets/0e60a248-e3c0-4c22-b0b2-28f123a64e4a" />


2️⃣ Attrition vs YearsSinceLastPromotion
<img width="753" height="526" alt="image" src="https://github.com/user-attachments/assets/c11730d6-6fab-4b3d-9437-eff3f999d6e9" />

3️⃣ Attrition vs YearsAtCompany
<img width="729" height="532" alt="image" src="https://github.com/user-attachments/assets/4b457b93-8eab-447b-81e0-db07c2a648a4" />


4️⃣ Matrice de corrélation (si possible)

Créer une matrice avec :

JobSatisfaction

EnvironmentSatisfaction

WorkLifeBalance

RelationshipSatisfaction

Attrition

<img width="635" height="435" alt="image" src="https://github.com/user-attachments/assets/2b8b8571-deab-489d-a284-68901fcf3ec2" />

👉 Identifier les variables critiques

# 2️⃣ Define (Définir le problème)

Après analyse, on pourrait définir le problème ainsi :

> “Les jeunes employés avec peu d’ancienneté, travaillant en heures supplémentaires et ayant peu d’opportunités de promotion présentent un risque élevé d’attrition.”

Ou plus globalement :

> “Le manque d’équilibre vie pro/perso et d’évolution de carrière est un facteur majeur de départ.”

On transforme donc le problème en :

🎯 **Comment améliorer la rétention des profils à risque ?**

---

# 3️⃣ Ideate (Générer des idées)

En se basant sur les variables du dataset :

## 💡 Idées d’actions RH

### Si `OverTime` est fortement lié à Attrition :

* Politique de réduction des heures supplémentaires
* Recrutement pour réduire la charge

### Si `YearsSinceLastPromotion` est critique :

* Plan de carrière personnalisé
* Promotion plus fréquente

### Si `WorkLifeBalance` est faible :

* Télétravail
* Horaires flexibles

### Si `MonthlyIncome` impacte :

* Revue salariale ciblée
* Bonus rétention

### Si `DistanceFromHome` joue :

* Politique hybride
* Aide transport

---

# 4️⃣ Prototype (Prototyper une solution Data)

À partir du dataset, on peut créer :

## 📊 1. Modèle prédictif d’attrition

* Logistic Regression
* Random Forest
* XGBoost

Objectif :
👉 Prédire la probabilité de départ d’un employé

---

## 📈 2. Dashboard RH

Indicateurs :

* Taux d’attrition par département
* Attrition par niveau de salaire
* Attrition vs Overtime
* Attrition par ancienneté

---

## 🎯 3. Score de risque individuel

Créer un **Attrition Risk Score** :

Exemple :

```
Risk Score = 
+ OverTime
+ Low JobSatisfaction
+ Low WorkLifeBalance
+ YearsSinceLastPromotion élevé
+ Faible salaire
```

---

# 5️⃣ Test (Tester et mesurer)

## 🔬 Expérimentation possible :

* Implémenter un programme pilote sur un département
* Mesurer :

  * Réduction du taux d’attrition
  * Amélioration satisfaction
  * Baisse OverTime

## 📊 KPI à suivre :

* Attrition Rate
* Engagement Score
* Temps moyen avant départ
* Taux de promotion interne

---

# 📌 Résultat final attendu

Un projet complet pourrait ressembler à :

1. Analyse exploratoire (EDA)
2. Identification des drivers de l’attrition
3. Modèle prédictif
4. Dashboard RH
5. Plan d’action RH basé data
6. Test & amélioration continue
