---
title: "RAG : Les leçons que personne ne partage (2026) (fr)"
date: 2026-04-05T11:26:46.632+02:00
category: videos
tags: [RAG, intelligence artificielle, extraction de données, interface utilisateur, gestion des données, Golden Dataset, évaluation de modèle, projet IA, data cleaning, embedding hybride]
excerpt: "En 2025, les projets RAG échouent souvent à cause de la qualité des données et de l'interface utilisateur. Ce guide détaille les vraies leçons terrain pour éviter ces erreurs et réussir son projet."
---

![thumbnail](https://i.ytimg.com/vi_webp/tGiCvd9I80U/maxresdefault.webp)
[https://youtu.be/tGiCvd9I80U?si=TdP9haFlB3DtfoqN](https://youtu.be/tGiCvd9I80U?si=TdP9haFlB3DtfoqN)

## My thoughts

Not specified (yet)

## TLDR;
- En 2025, l'expérience montre que 80 % des problèmes dans les projets RAG viennent de la qualité des données ou de l'interface utilisateur, pas du modèle.
- La mauvaise extraction de données, la présence de doublons, le bruit dans les données, l'absence de métadonnées et la donnée incomplète sont des freins majeurs.
- L'interface doit guider l'utilisateur pour qu'il formule correctement ses questions et fournisse le contexte nécessaire.
- Le Golden Dataset, un ensemble de 15 à 50 questions-réponses réelles, est indispensable pour évaluer la performance du RAG et définir la structuration de la donnée.
- Une configuration de base efficace combine un chunking naïf, un embedding hybride (sémantique + mots-clés) et un reranker pour extraire les informations les plus pertinentes.
- L'évaluation rigoureuse repose sur trois métriques clés : précision, rappel (recall) et fidélité à la source (faithfulness).
- Les erreurs fréquentes incluent le testing insuffisant, la sous-estimation de la data et de l'interface, l'over-engineering, ne pas auditer la data ni comprendre le périmètre précis, et promettre des délais irréalistes sans connaître la donnée.
- Le succès dépend de la preuve de valeur, pas simplement de la preuve de faisabilité technique, et il faut savoir quand ne pas faire de RAG pour éviter des projets voués à l'échec.



## Content

### Les véritables causes des échecs en projets RAG
En 2025, après avoir livré plus de 15 projets RAG avec un taux de déploiement de 93 %, il ressort que la majorité des problèmes ne viennent pas du modèle ou du chunking, mais plutôt de la qualité des données et de l'interface utilisateur. "80 % des problèmes viennent de la data ou de l'interface," souligne-t-il. Par exemple, des PDF mal extraits sans OCR manquent d’informations importantes, rendant le RAG inefficace. La présence de doublons dans les données, le bruit non filtré (où près de 70 % des données sont inutiles), l’absence de métadonnées et surtout les données incomplètes nuisent gravement à la pertinence des réponses.

### L'importance cruciale de l'interface utilisateur
Un RAG peut fonctionner parfaitement, mais si l’utilisateur ne sait pas formuler sa question ou quel niveau de contexte fournir, l’outil sera sous-utilisé. "Un RAG moyen avec une bonne interface bat toujours un RAG parfait avec une interface nulle." L'interface doit guider l'utilisateur pour qu'il puisse fournir le contexte nécessaire afin d'obtenir les bonnes réponses. Ce syndrome du chatbot magique, qui s'attend à ce que l'outil devine tout, est à éviter.

### Le Golden Dataset : outil clé de mesure et d’amélioration
Le Golden Dataset est une série de 15 à 50 questions-réponses réelles, recueillies avec les utilisateurs, permettant de mesurer la performance du système à différentes étapes et d'ajuster la structuration des données avec les métadonnées adéquates. On construit ce dataset avec trois niveaux de difficulté de questions, afin d’évaluer la pertinence des réponses et la qualité de la data. Une erreur majeure est d'inventer les questions soi-même sans connaître le besoin utilisateur, ce qui mène à des biais et à des défaillances.

### Une configuration de base efficace pour la majorité des PME
Avant de complexifier la solution, il recommandede structurer la donnée sémantiquement avec un chunking naïf, d’utiliser un embedding hybride combinant sémantique et mots-clés, et d’ajouter un reranker pour mettre en avant les informations les plus pertinentes. Cette baseline fonctionne bien dans 70 % des cas PME, permettant de mesurer les écarts de performance avant d’envisager des optimisations plus avancées.

### L’évaluation rigoureuse pour garantir la fiabilité
L’analyse précise repose sur trois critères essentiels :
- La précision : la réponse doit être complète, précise et répétable.
- Le rappel (recall) : le système doit retrouver les informations justes dans la base de connaissances.
- La fidélité (faithfulness) : la réponse doit être sourcée et fidèle aux données disponibles, évitant toute hallucination venant des données d'entraînement.
Un audit systématique via le Golden Dataset donne un score en pourcentage afin de valider la robustesse avant mise en production.

### Les erreurs fréquentes et comment les éviter
Les erreurs observées en 2025 sont multiples :
- Le syndrome YouTube : tester sur un petit jeu de données et lancer en production trop tôt.
- Ne mesurer que la faisabilité technique sans prouver la valeur business.
- Croire avoir toute la donnée sans l’auditer, ce qui mène à de mauvaises surprises en cours de projet.
- Vouloir tout faire d’entrée, sans périmètre clair, ce qui rend le projet ingérable.
- Sous-estimer l’importance de l’interface utilisateur, ce qui limite l’adoption.
- Over-engineering : construire des systèmes complexes et coûteux sans itérer sur la valeur réelle.
- Omettre l’audit de la donnée ou promettre des délais trop courts sans analyse préalable.

### L’essentiel pour réussir un projet RAG
"Les entreprises veulent du résultat, pas de la technologie." Le vrai enjeu est d’apporter une preuve de valeur, un retour sur investissement visible, et de savoir quand ne pas faire de RAG. Il faut savoir reconnaître les cas où le RAG n’apportera pas de valeur ajoutée et éviter de forcer sa mise en œuvre. La clarté sur la data, l’accompagnement utilisateur par une interface bien pensée, un audit précis, un Golden Dataset et une évaluation rigoureuse font la différence entre un projet réussi ou un échec.

### Conclusion
Les enseignements des deux dernières années montrent l’importance capitale de la qualité des données, de la conception d’interfaces utilisateur guidantes, de la rigueur dans l’évaluation et surtout de s’appuyer sur des tests réels avec les utilisateurs. Le RAG n’est qu’une brique parmi d’autres dans le succès d’un projet IA. Pour comprendre pourquoi 85 % des projets IA échouent, au-delà du RAG, une vidéo complète est disponible pour explorer ces pièges en amont.





> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/921](https://github.com/Nikoms/n8n/tree/main/ongoing/921)