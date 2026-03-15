# Liste de vérification des bonnes pratiques

## 1. Pensée système
1. Dessiner la vue d'ensemble
- Action : produire diagrammes de composants, flux, dépendances.
- Conseil : marquer les frontières et contrats.
2. Vérifier la cohérence globale
- Action : revoir nommage, style, gestion d'erreurs.
- Conseil : appliquer via revue ou outils.
3. Concevoir d'abord les frontières
- Action : définir responsabilités, interfaces, dépendances.
- Conseil : la complexité interne ne doit pas fuiter.

## 2. Modularité et couches
4. Séparer par fonction
- Action : isoler présentation, métier, données.
- Conseil : chaque couche a une responsabilité unique.
5. Forte cohésion, faible couplage
- Action : minimiser dépendances externes.
- Conseil : masquer l'implémentation par des interfaces.
6. Séparer bibliothèques communes et métier
- Action : isoler utilitaires communs.
- Conseil : éviter les dépendances circulaires.

## 3. Design progressif
7. Suivre YAGNI
- Action : implémenter uniquement le nécessaire.
- Conseil : évoluer quand les besoins changent.
8. Refactoriser régulièrement
- Action : simplifier les modules complexes.
- Conseil : garder les modules maintenables.
9. Boucle revue/feedback
- Action : faire des revues d'architecture par itération.
- Conseil : planifier des jalons réguliers.

## 4. Compréhensibilité et maintenabilité
10. Nommage clair
- Action : noms explicites pour classes/fonctions.
- Conseil : conventions d'équipe.
11. Interfaces simples
- Action : exposer le strict nécessaire.
- Conseil : documenter paramètres, retours, erreurs.
12. Patterns et templates
- Action : utiliser des patterns éprouvés.
- Conseil : réduire le design répétitif.

## 5. Expérience et feedback
13. Extraire des patterns de succès
- Action : analyser projets open-source ou internes.
- Conseil : viser réutilisable et scalable.
14. Analyser les échecs
- Action : documenter les causes racines.
- Conseil : créer une base de leçons apprises.
15. Mettre en place des revues
- Action : enregistrer les décisions et surveiller les performances.
- Conseil : faire des revues post-lancement.
