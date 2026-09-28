# Réponse - Exo 1 : La fenêtre nue

Le plus petit programme comporte **17 lignes** réparties ainsi :

* **Lignes 1-2 (`#include`) :** Inclusions indispensables. La ligne 2 (`NKMain.h`) évite l'erreur d'édition de liens `WinMain` en fournissant les points d'entrée natifs de chaque plateforme.
* **Ligne 4 (`nkmain`) :** Point d'entrée multiplateforme unifié par le module `NKWindow`.
* **Lignes 5-8 (`NkWindowConfig`) :** Configuration de la famille "identité et taille" de la fenêtre (titre, largeur, hauteur).
* **Ligne 10 (`NkWindow window`) :** Appel du constructeur qui instancie et crée physiquement la fenêtre à ce moment-là.
* **Lignes 11-14 (`if (!window.IsOpen())`) :** Sécurité indispensable qui vérifie la réussite de l'ouverture (pilote absent, permissions, etc.) pour éviter que le programme ne travaille dans le vide.
* **Ligne 15 (`while`) :** Boucle principale qui maintient la fenêtre ouverte et sert de point de passage pour la file d'événements.
* **Ligne 16 (`return 0`) :** Fin et fermeture propre du programme une fois la boucle quittée.
