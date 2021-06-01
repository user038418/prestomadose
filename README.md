# Presto Ma Dose

Outil de recherche automatisée de rendez-vous pour la vaccination contre la COVID-19

Les rendez-vous sont cherchés directement sur le site de Doctolib pour éviter tout temps de retard

## Utiliser sur Doctolib

Les instructions ci-dessous permettront de créer un bouton sur le site Doctolib qui lance la recherche automatique de rendez-vous

Une extension pour Firefox est en cours d'acheminement. La démarche d'utilisation sera alors bien plus simple.

1. **Ouvrir la page Doctolib d'un centre de vaccination**

2. **Copier ce code et lancez-le dans la console :**
   
    [Comment utiliser la console ?](https://github.com/user038418/prestomadose/#comment-utiliser-la-console-)

    ```javascript
    (() => {
        let script = document.createElement('script');
        script.src = "https://cdn.jsdelivr.net/gh/user038418/prestomadose@v2.2/dose_covid.js";
        document.body.appendChild(script);
    })();
    ```

3. **Sélectionnez une date, cliquez sur "Trouver un rendez-vous" et attendez !**
   
   Il vous sera probablement demandé d'accepter les notifications, vous devrez alors cliquer sur "Autoriser"
   
   Démonstration :
   
   ![Démonstration](img/demo.gif)

### Comment utiliser la console ?

1. **Cliquer sur `F12`**
   
   <img src="img/f12_key.webp" width="60%" alt="F12 Key">

2. **Cliquer sur l'onglet console**
   
   <img alt="DevTools Console" src="img/console.webp" width="60%">

3. **Coller le code ci-dessus**
   
   Sur Firefox, il est nécessaire de suivre les instructions affichées pour pouvoir coller le code dans la console
   
   <img alt="Coller le code" src="img/paste.webp" width="60%">


----
### Package Extension

Dans le dosier, lancer :
```
zip -r -FS prestomadose-<version number>.zip dose_covid.js manifest.json img/icon.png
```