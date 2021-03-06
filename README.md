# Dungeon Quizz

## Fonctionnement

### Main
Au départ, la scène Main est chargé, c'est ici qu'on va définir les variables et fonctions qui devront être disponible tout au long du jeu. Ensuite il charge automatique la première scène : **Menu**

### Menu
Le menu va appeler le provider qui s'occupe de récupérer les informations de l'API et de les transformer en objet C# sur l'url /quizzes. Ensuite pour chaque quizz, il va créer un bouton et aller chercher chaque quizz en ligne /quizzes/{id}, ce qui permet de ne plus faire aucun appel à l'API durant le reste de l'execution du jeu. Une fois que l'on clique sur le bouton d'un quizz, cela charge la scène **Quizz**

### Quizz
Le quizz va charger toutes les questions dans un tableau de questions "non-répondues", ensuite une question va être selectionnées aléatoirement dans ce tableau et affichée. Lors d'un clic sur une réponse, le script va contrôler si c'est la bonne réponse ou pas puis l'afficher. Cela permettra de définir le niveau (Easy ou Hard) du Jeu et charger la scène **Game**

### Game

## Fichiers

Classes :
* **Answer** permet de transformer une réponse JSON en objet
* **Quizz** permet de transformer un quizz JSON en objet
* **Quizzes** permet de transformer un élément du list de quizzes JSON en objet
* **Question** permet de transformer une question JSON en objet

Managers :
* **MainManager** est le manager principale
* **MenuManager** permet de gérer la scène menu
* **QuizzManager** permet de gérer la scène Quizz
* **GameManager** permet de gérer la scène Game

Autres :
* **Provider** s'occupe de faire les appels à l'API et de transformer le JSON en objet

## Tutoriels
* [Quizz in Unity](https://www.youtube.com/watch?v=g_Ff1SPhidg&list=PLPV2KyIb3jR7ucA2yo5pjvKY0cJmNTq2L)
* [Customize text (Textmesh Pro)](https://assetstore.unity.com/packages/essentials/beta-projects/textmesh-pro-84126)
* [Dynamique quizz bouton avec scroll](http://gregandaduck.blogspot.com/2015/07/unity-ui-dynamic-buttons-and-scroll-view.html)

## Auteurs
* Kévin
* Benjamin
