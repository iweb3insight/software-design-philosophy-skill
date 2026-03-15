# Méthodologie de design (actionnable)

## 1. Pensée système
- Principe : le design concerne l'ensemble du système.
- Méthodes :
1. Dessiner tôt la vue d'ensemble (composants, flux de données, dépendances).
2. Prioriser les frontières claires et les contrats d'interface.
3. Vérifier la cohérence globale (style, nommage, erreurs).
- Exemple : les grands projets open-source définissent tôt les frontières et contrats.

## 2. Modularité et couches
- Principe : modularité claire, couplage faible.
- Méthodes :
1. Séparer par fonction et dépendance (présentation, métier, données).
2. Forte cohésion interne, faible couplage externe.
3. Séparer bibliothèques communes et bibliothèques métier.
- Exemple : séparation stricte entre accès aux données et logique métier.

## 3. Design progressif
- Principe : le design évolue avec les besoins.
- Méthodes :
1. Éviter la surconception (YAGNI).
2. Refactoriser régulièrement les modules clés.
3. Ajuster via revues et feedback utilisateurs.
- Exemple : les frontières microservices se raffinent par itérations.

## 4. Compréhensibilité et maintenabilité
- Principe : code et docs sont des outils de communication.
- Méthodes :
1. Nommage clair et sans ambiguïté.
2. Interfaces simples, complexité cachée.
3. Utiliser des patterns et des templates.
- Exemple : frameworks comme Django faciles à adopter grâce à des API claires.

## 5. Expérience et boucle de feedback
- Principe : le design s'améliore par la pratique.
- Méthodes :
1. Extraire des patterns de cas réussis.
2. Analyser les échecs (cause racine).
3. Mettre en place décisions, revues, monitoring.
- Exemple : revues d'architecture régulières dans les systèmes commerciaux.
