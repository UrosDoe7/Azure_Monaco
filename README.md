# Azure_Monaco_Shell
Pulling Monaco image on docker - create multiple HTTPmonitor Synthetic 

Step 1 : créer les variables d'environnements dans le fichier env.sh qui permettront à variabiliser le YAML pour exécution.

Step 2 : JSON pour donner forme/structure via la pipeline CI/CD; Alimenter avec les variables YAML le JSON qui sera à requêter.
         Exemple : avec le "name":"{{.name}}"
         
Step 3 : Edition du shell "loop.sh", afin de créer une boucle sur les urls qui feront office chacunes de scénarios HTTPMonitor Synthetic.

NotaBene: pour de plus d'exercices et template MONACO https://github.com/JLLormeau/lab-environment-for-dynatrace-training#lab-environment-for-dynatrace-training

##### Dashboard results via MONACO
![image](https://user-images.githubusercontent.com/63231022/162389601-31bb287f-04ac-44f1-b7b4-12959ea1f2c0.png)

