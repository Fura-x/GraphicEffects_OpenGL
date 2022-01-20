# Projet Effets graphiques  

Groupe de Lancelot BL, Rayane et Florian.  
Le projet consiste à travailler sur divers effets graphiques visant à rendre notre jeu plus beau ou plus original. Nous avons choisi de présenter la **Skybox avec réflexion dynamique/réfraction**. Nous nous sommes aussi concentré sur le **HDR _(High dynamic range)_**.  

## Bilan des effets réalisés  
- Skybox
- Réflexion dynamique
- Réfraction (non-utilisé)  
- Gamma correction  
- HDR  
- Bloom _(Notion de 'pingpong'/'blur')_ 
- Post processing simple _( échelle de gris, inverse, matrice de Kernel)_  
- Instancing  
- Normal mapping  
  
## Organisation des Demo  
Le moteur utilisé fonctionne sur un système de scène appelé 'demo'. Il est possible de changer de demo via la fenêtre ImGui, sur laquelle de nombreuses options de Debug/Edition sont accessibles.  
La première scène est une démonstration de la Skybox et de la réflexion dynamique.  
La seconde regroupe la quasi-totalité des effets mais avec de nombreux défauts.  
Les suivantes sont une séparation des effets réalisés.  

## Problèmes rencontrés  
- La réflexion dynamique ne marche pas correctement dans demo_full  
- Le bloom peut-être appliqué sur les éléments autre que la taverne de manière incorrect.  
- Les instances _(météorites)_ reçoivent toute la même lumière.  
- L'ambiante des lumières agis étrangement. Si une scène semble trop blanchie, c'est qu'il faut éteindre la couleur ambiante des lumières.  
- L'HDR et le Post process avec une matrice Kernel ne sont pas compatibles. C'est soit l'un soit l'autre.  
- Il peut y avoir une erreur dans la fenêtre de commande lors de la fermeture du programme. Le problème est lié à la scène de la skybox, mais impossible de déterminer la source.