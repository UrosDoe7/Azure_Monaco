# Azure_Monaco_Shell
Pulling Monaco image on docker - create multiple HTTPmonitor Synthetic 

Step 1 : créer les variables d'environnements dans le fichier env.sh qui permettront à variabiliser le YAML pour exécution.

Step 2 : JSON pour donner forme/structure via la pipeline CI/CD; Alimenter avec les variables YAML le JSON qui sera à requêter.
         Exemple : avec le "name":"{{.name}}"
         
Step 3 : Edition du shell "loop.sh", afin de créer une boucle sur les urls qui feront office chacunes de scénarios HTTPMonitor Synthetic.

NotaBene: pour de plus d'exercices et template MONACO https://github.com/JLLormeau/lab-environment-for-dynatrace-training#lab-environment-for-dynatrace-training

##### Dashboard results via MONACO
![image](https://user-images.githubusercontent.com/63231022/162389601-31bb287f-04ac-44f1-b7b4-12959ea1f2c0.png)

get Dashboard 
2. stocké dans gitlab project , un sous dossier contenant les Jsons 
3. variabiliser les JSON par le YAML
4. (action unique) installer monaco via le lien officiel Github
5. créer un environment.yaml pour les variables d'environnements et interfacer avec Dynatrace (NEW_CLI / MyTenant/ MyToken)

finaliser l'action en CLI : ./monaco deploy -e=environment.Yaml nomduFichier_contenant_JSON



