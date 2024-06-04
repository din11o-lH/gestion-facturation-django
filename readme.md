# Titre du Projet

Système de Gestion de Facturation Django

## Description

Ce projet est une application web basée sur Django conçue pour gérer les clients, les factures et les articles. Elle fournit des modèles pour la gestion des informations des clients, la génération de factures et la gestion des articles au sein des factures.

## Modèles

### Client (Customer)

Représente les informations des clients.

- **Champs :**
  - `name`: Nom du client (longueur maximale : 132).
  - `email`: Adresse email du client.
  - `phone`: Numéro de téléphone du client (longueur maximale : 20).
  - `adress`: Adresse du client (longueur maximale : 64).
  - `sex`: Sexe du client (choix : 'Masculin', 'Feminin').
  - `age`: Âge du client (longueur maximale : 12).
  - `city`: Ville du client (longueur maximale : 12).
  - `zip_code`: Code postal du client (longueur maximale : 16).
  - `create_date`: Date de création du client (définie automatiquement).
  - `save_by`: Utilisateur ayant enregistré le client.

### Facture (Invoice)

Représente une facture liée à un client.

- **Champs :**
  - `customer`: Clé étrangère vers le modèle Customer.
  - `save_by`: Utilisateur ayant enregistré la facture.
  - `invoice_date_time`: Date et heure de création de la facture (définie automatiquement).
  - `total`: Montant total de la facture.
  - `last_updated_date`: Date de la dernière mise à jour de la facture (optionnel).
  - `paid`: Booléen indiquant si la facture est payée.
  - `invoice_type`: Type de facture (choix : 'Reçu', 'Proforma facture', 'Facture').
  - `comment`: Commentaires supplémentaires sur la facture (optionnel, longueur maximale : 1000).

### Article

Représente un article dans une facture.

- **Champs :**
  - `invoice`: Clé étrangère vers le modèle Invoice.
  - `name`: Nom de l'article (longueur maximale : 32).
  - `quantity`: Quantité de l'article.
  - `unit_price`: Prix unitaire de l'article.
  - `total`: Prix total de l'article.

## Démarrage

### Prérequis

- Python 3.x
- Django 3.x ou supérieur

### Installation

1. Clonez le dépôt :

    ```bash
    git clone https://github.com/din11o-lH/gestion-facturation-django.git
    ```

2. Accédez au répertoire du projet :

    ```bash
    cd gestion-facturation-django
    ```

3. Installez les dépendances requises :

    ```bash
    pip install -r requirements.txt
    ```

4. Appliquez les migrations :

    ```bash
    python manage.py migrate
    ```

5. Créez un superutilisateur :

    ```bash
    python manage.py createsuperuser
    ```

6. Lancez le serveur de développement :

    ```bash
    npm run build:css
    python manage.py runserver
    ```

7. Accédez à l'application à l'adresse `http://127.0.0.1:8000/`.

## Utilisation

- Utilisez l'interface d'administration Django pour gérer les clients, les factures et les articles.
- Créez des clients et liez-les aux factures.
- Ajoutez des articles aux factures et gérez leurs détails.

## Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

## Auteur

Dino

Pour toute question ou support, veuillez contacter Dino à [ndimbiarisoadino@gmail.com].

## Contribution

Les contributions sont les bienvenues ! Veuillez forker le dépôt et soumettre une pull request avec vos modifications.

## Remerciements

- Documentation Django : https://docs.djangoproject.com/
- OpenAI pour l'assistance avec la configuration du projet et la documentation.

---

