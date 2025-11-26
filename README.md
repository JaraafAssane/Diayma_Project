

===========================================================================================



&nbsp;Rapport du projet Diayma


## TÂCHE 2 : Projets de la Solution

La solution contient 1 projet :

\- \*\*Diayma\*\* : Application web ASP.NET Core MVC



## TÂCHE 3 : Version SDK

\- Version originale du projet : .NET Core 2.0 (netcoreapp2.0)

\- Version mise à jour : .NET 10.0 (net10.0)



&nbsp;
## TÂCHE 4 : Installation SDK

Le SDK .NET 10.0 a été installé et le projet a été migré de la version 2.0 vers la version 10.0.


https://github.com/JaraafAssane/Diayma_Project.git

## TÂCHE 6 : Exploration et Bugs

J'ai exploré l'application et identifié les bugs suivants :



1\. Bug de navigation (Panier) :

&nbsp;  Lorsqu'on ajoute un produit au panier et qu'on clique sur "Continue shopping", l'application nous redirige vers la page d'accueil (tous les produits) au lieu de nous ramener à la catégorie ou la page que nous consultions précédemment.



2\. Bug de validation (Commande) :

&nbsp;  Lorsqu'on tente de valider une commande (Checkout) sans remplir aucun champ, l'application plante (génère une exception) au lieu d'afficher des messages d'erreur demandant de remplir les champs obligatoires.





## TÂCHE 7/8 : Analyse de l'exécution (Débogage)

Lors du lancement de l'application et de l'affichage de la page d'accueil, voici l'ordre d'exécution observé via les points d'arrêt :



1\. Initialisation

&nbsp;  - Namespace :Diayma

&nbsp;  - Classe : Startup

&nbsp;  - Méthode : Constructeur `Startup(IConfiguration configuration)`

&nbsp;  - Description :L'application démarre et charge la configuration initiale.



2\. Traitement de la requête (Page d'accueil)

&nbsp;  - Namespace : Diayma.Controllers

&nbsp;  - Classe : ProductController

&nbsp;  - Méthode :`Index()`

&nbsp;  - Description : Le contrôleur reçoit la demande d'affichage par défaut. Il interroge la base de données pour récupérer la liste des produits (`GetAllProducts`) et prépare la vue.



3\. Affichage des composants (Panier)

&nbsp;  - Namespace : Diayma.Components

&nbsp;  - Classe : CartSummaryViewComponent

&nbsp;  - Méthode : `Invoke()` (appelée après le constructeur)

&nbsp;  - Description : Pendant que la page se dessine, la vue appelle ce composant pour afficher le résumé du panier (icône et total) intégré dans la mise en page.




## TÂCHE 9 : Exécutable du projet
Voici le lien pour télécharger la version déployée (.exe) de l'application :
[Télécharger l'application (Google Drive)](https://drive.google.com/file/d/1RvnnareaMEccsweqxPRwsDq8YYu2f9fe/view?usp=sharing)


















