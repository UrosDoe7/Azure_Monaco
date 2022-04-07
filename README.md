# Azure_Monaco_Shell
Pulling Monaco image on docker - create multiple HTTPmonitor Synthetic 

Step 1 : créer les variables d'environnements dans le fichier env.sh qui permettront à variabiliser le YAML pour exécution.

Step 2 : JSON pour donner forme/structure via la pipeline CI/CD; Alimenter avec les variables YAML le JSON qui sera à requêter.
         Exemple : avec le "name":"{{.name}}"
         
Step 3 : Edition du shell "loop.sh", afin de créer une boucle sur les urls qui feront office chacunes de scénarios HTTPMonitor Synthetic.
