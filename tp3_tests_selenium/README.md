# TP3 – Tests automatisés avec Selenium

## 🎯 Objectif pédagogique
Ce TP a pour but de vous familiariser avec les tests automatisés d'interfaces web en utilisant Selenium WebDriver. À travers ce projet, vous apprendrez à :

### Objectifs d'apprentissage
- **Automatiser des tests d'interface utilisateur** avec Selenium WebDriver
- **Interagir avec les éléments web** (champs de formulaire, boutons, messages)
- **Valider le comportement attendu** d'une application web
- **Gérer différents scénarios de test** (cas positifs, négatifs, cas limites)
- **Organiser des tests automatisés** de manière structurée

## 📋 Description du TP
Ce projet comprend une application Flask simple avec un système d'authentification et des tests automatisés Selenium qui vérifient son bon fonctionnement. C'est un exemple pratique pour comprendre comment :

1. **Configurer Selenium** avec Python
2. **Écrire des tests automatisés** pour une application web
3. **Valider les interactions utilisateur** et les messages d'erreur
4. **Automatiser** des scénarios de test courants

## 🧪 Détail des tests implémentés

### 1. Test de connexion réussie
- **Objectif** : Vérifier qu'un utilisateur peut se connecter avec des identifiants valides
- **Cas testé** : Saisie du nom d'utilisateur et du mot de passe valides
- **Validation** : Redirection vers la page du tableau de bord après connexion

### 2. Test d'échec de connexion
- **Objectif** : Vérifier que le système rejette les identifiants invalides
- **Cas testé** : Saisie d'un nom d'utilisateur ou mot de passe incorrect
- **Validation** : Affichage d'un message d'erreur approprié

### 3. Test de champs vides
- **Objectif** : Vérifier la validation des champs obligatoires
- **Cas testé** : Soumission du formulaire sans saisir d'identifiants
- **Validation** : Affichage d'un message demandant de remplir tous les champs

## 🛠️ Compétences techniques développées
- Utilisation de Selenium WebDriver avec Python
- Localisation d'éléments web (ID, classe, XPath, etc.)
- Gestion des attentes explicites et implicites
- Gestion des exceptions dans les tests
- Organisation des tests avec pytest

## 🚀 Instructions
1. Installe les dépendances :
   pip install -r requirements.txt

2. Lance l'app :
   python app/app.py

3. Dans un autre terminal :
   pytest tests/test_login.py


##---

# TP3 – Tests automatisés avec Selenium

## 🎯 Objectif
Automatiser des scénarios de test avec Selenium sur une application Flask de login.

## 📋 Description
Ce projet est une application web de démonstration avec des tests automatisés Selenium. Il comprend :
- Une application Flask simple avec une page de connexion
- Des tests automatisés pour différents scénarios de connexion
- Une configuration prête à l'emploi avec Selenium WebDriver

## 🚀 Prérequis
- Python 3.7+
- pip (gestionnaire de paquets Python)
- Navigateur Chrome installé
- ChromeDriver (sera installé automatiquement via les dépendances)

## ⚙️ Installation

1. **Cloner le dépôt**
   ```bash
   git clone [URL_DU_DEPOT]
   cd tp3_tests_selenium
   ```

2. **Créer et activer un environnement virtuel**
   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Sur Windows
   source venv/bin/activate  # Sur macOS/Linux
   ```

3. **Installer les dépendances**
   ```bash
   pip install -r requirements.txt
   ```

## 🏃‍♂️ Utilisation

1. **Lancer l'application Flask** (dans un premier terminal)
   ```bash
   python app/app.py
   ```

2. **Exécuter les tests** (dans un second terminal)
   ```bash
   pytest tests/test_login.py -v  # -v pour un affichage détaillé
   ```

## 🧪 Scénarios de test

1. **Test de connexion réussie**
   - Vérifie qu'une connexion avec des identifiants valides redirige vers le tableau de bord

2. **Test d'échec de connexion**
   - Vérifie qu'une erreur s'affiche avec des identifiants invalides

3. **Test de champs vides**
   - Vérifie que le formulaire affiche une erreur quand des champs requis sont vides

## 📁 Structure du projet
```
tp3_tests_selenium/
├── app/
│   ├── __init__.py
│   ├── app.py          # Application Flask principale
│   └── templates/
│       └── login.html  # Template de la page de connexion
├── tests/
│   └── test_login.py  # Tests Selenium
├── requirements.txt    # Dépendances Python
└── README.md          # Ce fichier
```

## 🔍 Résolution des problèmes

Si vous rencontrez des erreurs liées à ChromeDriver :
1. Assurez-vous que Chrome est installé
2. Vérifiez que la version de Chrome correspond à celle de ChromeDriver dans `requirements.txt`
3. Si nécessaire, mettez à jour Chrome ou spécifiez une version compatible de ChromeDriver

## 📝 Notes
- Les identifiants par défaut sont : `admin` / `password123`
- L'application tourne sur `http://localhost:5000/login` par défaut