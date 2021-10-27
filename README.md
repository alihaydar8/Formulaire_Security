# formulaire

# composer install
pour installer les bibliothèques requises par le projet

# Configurer le fichier .env
-mise a jour de la variable DATABASE_URL
-pour moi DATABASE_URL="mysql://root:@127.0.0.1:3306/formulaire"

# php bin/console doctrine:database:create
-pour creer la base de donnée formulaire

# php bin/console doctrine:migrations:migrate
-pour lancer les migrations sachant que mon tableau user est vide car j'ai eu du mal pour l'insertion du mots passe hasher
-donc c'est a vous de creer un mots de passe dans la partie inscription avant de hacker mon site :) ou lancer cette query dans la base (password:aHaydarhaydar8998) :
INSERT INTO `user` (`id`, `identifiant`, `roles`, `password`) VALUES
(10, 'alihaydar8', '[]', '$2y$13$e5XuLJNurQUqUAXixRsLzO7Rmjnj25.rxUd1nIwg3wu.pNaOeUgZ2');

# php -S localhost:8000 -t public
-finalement lancer le serveur 

##############################################################
-le projet est en php avec le framework symfony a l'aide de symfony j'ai créer la route de login et logout ....
-le mots de passe est hacher avec l’algorithme bcrypt et j'ai ajouté quelque contrainte de création de mots de passe
