Pour ex�cuter les exemples il est n�cessaire d'ajouter des d�pendences
vers les jars bpmnEngine_client.jar et w4Common_client.jar.
Il est n�cessaire �galement d'avoir un BPMN+ Engine � disposition.

Pensez � �diter les param�tres de connexion vers le serveur dans l'interface SampleConstants (dans le cas
o� l'installation du moteur n'utilise pas les param�tres par d�faut).

Un fichier BPMN est joint dans resources/eu/w4/sample/MyFirstBpmn.bpmn
L'image bpmn.png illustre le processus mod�lis�.

L'ordre logique de d�couverte des exemples est :
- ConnectionAndAuthentication
- CreateUser (ex�cutable une seule fois, d�s la seconde ex�cution une erreur se produira indiquant que l'utilisateur existe d�j�)
- SendBpmnToServer (ex�cutable une seule fois, d�s la seconde ex�cution un erreur indiquera que le BPMN est d�j� import�)
- BpmnRuntimeStuff (n�cessite l'ex�cution pr�alable du test SendBpmnToServer ou l'envoi du BPMN MyFirstBpmn.bpmn sur le serveur par un autre moyen)
- SearchUserTasks
