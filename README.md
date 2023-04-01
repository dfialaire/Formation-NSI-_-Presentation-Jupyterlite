Tutoriel
Utilisation de Jupyterlite
Fialaire David 2023.

I.	Créer une Github Page Jupyterlite :
( = un Site / Dashboard Notebooks en ligne )
A.	Initialisation :
1.	Se connecter à votre compte Github,
2.	Ouvrir, dans un autre onglet, ce lien : https://github.com/jupyterlite/demo
3.	Cliquer sur le bouton : Use this template  Create a new repository
 
4.	Renseigner : - Nom du repository, et cliquer sur : Create.
5.	Dans le Menu Horizontal : cliquer sur : Setting
a.	Dans le menu latéral : cliquer sur Pages
i.	Dans la section : Build and deployment / Source :
Transformer : Deploy from a branch  GitHub Actions
6.	Dans le Menu Horizontal : cliquer sur : Actions
	Vous observez des commits (Initial commits) en rouge : cliquer sur le 1er,
o	En haut à droite, cliquer sur : Re-Run jobs :
	Re-Run failled jobs  Re-run jobs
•	Attendre qu’il passe au vert..
7.	Dans le Menu Horizontal : cliquer sur Code
a.	Cliquer sur le dossier content,
i.	Cliquer sur Add File  Upload File :
1.	Déposer un/plusieurs notebooks, …des fichiers annexes..
	N’oubliez pas de commiter (en bas)
8.	Retourner dans le Menu Horizontal/Actions
a.	Suivez le Build/deployment de votre commit (il doit passer au vert)
9.	Dans le Menu Horizontal : cliquer sur : Setting
a.	Dans le menu latéral : cliquer sur Pages
 Vous observez le lien de votre Github Page Jupyterlite !




B.	Travail sur les bibliothèques nécessaires à vos Notebooks :
1.	Dans le Menu Horizontal : cliquer sur : Code,
a.	Cliquer sur :  requirement.txt,
i.	Et cliquer à droite sur le crayon (pour éditer) :
•	Si le module dont vous avez besoin n’est pas dans cette liste, rajoutez-le ;
	N’oubliez pas de Commiter et de suivre le bon deployment dans Actions.
•	Si le module dont vous avez besoin est déjà dans cette liste et que votre notebook ne fonctionne pas dans Github Page jupyterlite..
 Dans votre notebook, avant la cellule de code d’import :
import XXXX

créer une nouvelle cellule de code :
%pip install -q XXXX

Remarque 1 : L’utilisateur du Notebook sera donc amené à initialement « installer » (dans le navigateur Web uniquement !) le package qui posait un problème en activant la cellule : %pip install -q XXXX.

Remarque 2 : vous avez 2 possibilités pour modifier votre Notebook :
a)	Soit vous le modifier localement avec votre éditeur préferré, puis vous l’uploadez dans le repository/content ; vous Commitez et suivez le bon deployment.
b)	Soit vous l’éditez avec l’éditeur en ligne de Notebooks de Github : 
	Commencez par ouvrir votre Notebook à partir de votre repository/content ; puis cliquez sur la flèche, à droite du crayon, sur Open in GitHub Dev ; Dès lors, faîtes vos modif ; Pour Commiter, il vous suffit de faire Ctrl m, vous écrivez un commentaire de commit, puis vous faîtes Ctrl Entrée ; N’oubliez pas de suivre le bon deployment dans Actions.

