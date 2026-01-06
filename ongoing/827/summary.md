---
title: "RAG : Les leçons que personne ne partage (2026) (fr)"
date: 2026-01-06T09:55:14.680+01:00
category: videos
tags: [RAG, Data Quality, Interface Utilisateur, Golden Dataset, IA, Retrieval-Augmented Generation, Evaluation, PME, Best Practices]
excerpt: "Leçons essentielles tirées de plus de 15 projets RAG en 2025 : l'importance de la qualité des données, de l'interface utilisateur, du Golden Dataset et des erreurs à éviter pour réussir son projet IA."
---

![thumbnail](https://i.ytimg.com/vi/tGiCvd9I80U/maxresdefault.jpg)
[https://youtu.be/tGiCvd9I80U?si=aS9d-Hsq1I6gMsg_](https://youtu.be/tGiCvd9I80U?si=aS9d-Hsq1I6gMsg_)

<!--- My thoughts -->

## Content

### Introduction
En 2025, après avoir livré plus de 15 projets retrieval-augmented generation (RAG) avec un taux de déploiement de 93 %, il a partagé les leçons terrain rarement évoquées ailleurs. Ces enseignements ont permis d'éviter jusqu'à six mois de difficultés dans la mise en œuvre des projets.

### Problèmes majeurs dans les projets RAG
Il est courant de supposer que les difficultés viennent du modèle ou de la façon dont les données sont segmentées (« chunking »). Cependant, 80 % des problèmes sont liés à la qualité des données ou à l'interface utilisateur.

Côté données, les erreurs fréquentes incluent :
- Extraction de PDF sans OCR, ce qui entraîne des données incomplètes et des recherches inefficaces.
- Présence de doublons où il faut déterminer l'information maître.
- Bruit dans les données, avec souvent seulement 30 % de données utiles.
- Absence de métadonnées qui complique la pertinence des réponses.
- Données incomplètes qui rendent certaines questions impossibles à répondre.

### Importance de l'interface utilisateur
Même si le RAG fonctionne parfaitement en backend, un utilisateur mal guidé ne saura pas formuler ses questions efficacement, bloquant ainsi l'adoption. L'interface doit guider pour récolter le contexte suffisant et éviter le « syndrome du chatbot magique », où les utilisateurs attendent que l'IA devine leurs besoins.

### Le Golden Dataset, un outil clé
Le "Golden Dataset" est un jeu de 15 à 50 questions-réponses représentatives des besoins utilisateurs. Il sert à :
- Mesurer la performance du RAG.
- Définir le modèle de données adapté avec métadonnées.
- Évaluer la performance avant déploiement par des tests utilisateurs réels.

Pour construire ce dataset, il faut incorporer des questions faciles, moyennes et difficiles, définir la structure des réponses, et s'assurer qu'une personne connaissant bien le domaine valide la pertinence des réponses. Il est crucial de ne pas inventer soi-même les questions sans comprendre le besoin utilisateur.

### Configuration recommandée pour PME
Une configuration efficace comprend :
- Une structuration sémantique simple des données permettant un chunking naïf.
- Un embedding hybride combinant sémantique et mots-clés.
- Un re-ranker pour prioriser les chunks les plus pertinents.

Cette configuration couvre 70 % des cas PME et sert de base avant de complexifier.

### L’évaluation rigoureuse
L’évaluation doit dépasser les approximations visuelles, et s'appuyer sur trois critères :
- Précision : réponses précises, complètes, et répétables.
- Recall : système retrouve les chunks pertinents.
- Faithfulness : fidélité des réponses aux sources, évitant les hallucinations.

Un bon système doit être testé à grande échelle pour éviter les erreurs sporadiques impactant la fiabilité.

### Erreurs fréquentes observées en 2025
1. **Syndrome YouTube** : tester sur peu de documents et mettre en production prématurément.
2. Mesurer la faisabilité technique mais pas la valeur business.
3. Penser posséder toutes les données sans audit, menant à 60 % de données inutilisables.
4. Vouloir tout faire d’emblée, avec des périmètres trop larges et non gérables.
5. Sous-estimer l’importance de l’interface utilisateur qui freine l’adoption.
6. Côté fournisseurs, over engineering qui retarde l'itération sur ce qui compte vraiment.
7. Ne pas proposer ou faire d’audit de données.
8. Promettre des délais courts sans analyse préalable des données.

### Leçons clés
Les entreprises veulent des résultats business tangibles, pas juste des preuves de concept techniques. Il est tout aussi important, voire plus, de savoir quand ne pas faire de RAG pour éviter des projets inutiles.

Le RAG est une brique parmi d'autres dans l'écosystème IA. Pour comprendre pourquoi 85 % des projets IA échouent et comment l’éviter, une approche globale est nécessaire, envisageant data, interface, usage et évaluation.

### Conclusion
Les expériences des deux dernières années montrent l’importance capitale de la qualité des données, de l’interface utilisateur, et des bonnes pratiques méthodologiques. Grâce à ces enseignements, on peut significativement améliorer la réussite des projets RAG et IA en général.
