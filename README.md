# GestionEtudiants 📱

Application Android développée dans le cadre d'un lab de développement mobile pour apprendre la gestion d'une **base de données SQLite embarquée**.

---

## 🎯 Objectifs

- Créer un modèle métier `Etudiant`
- Initialiser une base SQLite locale avec `SQLiteOpenHelper`
- Implémenter des opérations CRUD via un service dédié
- Tester les services via Logcat
- Développer une interface simple (Ajouter, Chercher, Supprimer)

---

## 🏗️ Structure du projet

```
projet.fst.ma.app/
├── classes/
│   └── Etudiant.java             # Modèle métier (POJO)
├── util/
│   └── MySQLiteHelper.java       # Initialisation de la base SQLite
├── service/
│   └── EtudiantService.java      # Opérations CRUD
└── MainActivity.java             # Activité principale + interface utilisateur
res/
└── layout/
    └── activity_main.xml         # UI : Ajouter / Chercher / Supprimer
```

---

## ⚙️ Fonctionnement

| Action | Résultat |
|--------|----------|
| Saisir Nom + Prénom → **Valider** | Insère l'étudiant en base |
| Saisir un ID → **Chercher** | Affiche le Nom et Prénom |
| Saisir un ID → **Supprimer** | Supprime l'étudiant de la base |
| ID vide ou introuvable | Toast d'erreur affiché |

---

## 🧩 Concepts clés

- **`SQLiteOpenHelper`** — gère la création et la mise à jour de la base
- **`ContentValues`** — prépare les données avant insertion/mise à jour
- **`Cursor`** — itérateur sur les résultats d'une requête SQLite
- **`onCreate()`** — création de la table au premier lancement
- **`onUpgrade()`** — mise à jour de la base si la version change
- **`Toast`** — message temporaire non-bloquant affiché à l'écran
---

## Démonstration 
> https://github.com/user-attachments/assets/5eae17af-33d7-4c01-a3a2-0c767f6ba195

--- 
## 🛠️ Technologies utilisées

- **Langage** : Java
- **Base de données** : SQLite (embarquée Android)
- **Min SDK** : API 24 (Android 7.0)
- **IDE** : Android Studio
- **Template** : Empty Views Activity

---

## 👤 Auteur

**DOSSAH Yao Landry**  
ENSA Marrakech — GCDSTE (S4)  
Module : Programmation Mobile Android avec Java
