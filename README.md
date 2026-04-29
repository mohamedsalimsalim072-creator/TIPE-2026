# TIPE — Détection d’anomalies dans un réseau informatique

## Sujet

Comment détecter automatiquement un comportement anormal dans un réseau informatique ?

---

## Contexte

Les réseaux informatiques transportent une grande quantité de données et peuvent être la cible d’attaques ou de comportements anormaux (scan de ports, DDoS, etc.).

La détection de ces anomalies est essentielle pour garantir la sécurité et le bon fonctionnement des systèmes.

---

## Problématique

Comment concevoir un algorithme capable de détecter automatiquement des anomalies dans un trafic réseau tout en minimisant :

* le temps de calcul
* l’utilisation des ressources
* le nombre de fausses alertes

---

## Méthodes étudiées

Trois approches sont comparées :

* Méthode par seuil
* Méthode statistique
* Méthode par graphe

---

## Lien avec le thème

* **Sobriété** : réduction du coût en temps et en mémoire
* **Efficacité** : précision de la détection
* **Optimisation** : compromis entre performance et ressources

---

## Organisation du projet

* `src/` : codes C des différentes méthodes
* `data/` : données de trafic simulé
* `docs/` : documentation des méthodes et résultats

---

## Auteur

Projet réalisé dans le cadre du TIPE MP2I.
# Sprint 1 — Implémentation comparative

## Objectif

Comparer plusieurs méthodes de détection d’anomalies afin d’évaluer leur efficacité et leur coût.

---

## Méthodes

* Méthode par seuil
* Méthode statistique
* Méthode par graphe

---

## Données

Le trafic réseau est simulé via un fichier CSV.

Deux types de scénarios sont étudiés :

* trafic normal
* trafic anormal

---

## Métriques

* précision
* faux positifs
* temps d’exécution
* mémoire

---

## Lien avec le thème

* Sobriété : coût de calcul
* Efficacité : qualité de détection
* Optimisation : compromis entre les deux

---

## Conclusion

Ce sprint permet d’obtenir une première comparaison entre différentes méthodes.
# Méthode par seuil

## Principe

Une machine est considérée comme anormale si son nombre de connexions dépasse un seuil fixé.

---

## Avantages

* simple
* rapide
* peu coûteuse

---

## Limites

* dépend du seuil
* peu précise

---

## Conclusion

Méthode de base servant de référence.

# Méthode statistique

## Principe

On utilise la moyenne et l’écart-type pour détecter les valeurs anormales.

---

## Règle

si valeur > moyenne + 2 × écart-type → anomalie

---

## Avantages

* plus précise que seuil
* s’adapte aux données

---

## Limites

* sensible aux valeurs extrêmes

---

## Conclusion

Bon compromis entre simplicité et efficacité.

# Méthode par graphe

## Principe

Le réseau est modélisé par un graphe :

* sommets = machines
* arêtes = communications

Une machine est anormale si son degré est trop élevé.

---

## Avantages

* très efficace
* lien avec les mathématiques

---

## Limites

* plus coûteuse

---

## Conclusion

Méthode avancée offrant une meilleure détection.
# Comparaison des méthodes de détection d’anomalies

## Tableau comparatif

| Méthode     | Principe                        | Efficacité | Temps d'exécution | Mémoire     | Faux positifs | Complexité  |
| ----------- | ------------------------------- | ---------- | ----------------- | ----------- | ------------- | ----------- |
| Seuil       | Comparaison à une valeur limite | Faible     | Très rapide       | Très faible | Élevé         | Très faible |
| Statistique | Moyenne + écart-type            | Moyenne    | Rapide            | Faible      | Moyen         | Faible      |
| Graphe      | Analyse du degré des sommets    | Élevée     | Plus lent         | Moyenne     | Faible        | Moyenne     |

---

## Analyse des résultats

La méthode par seuil est très rapide et peu coûteuse en ressources, mais elle manque de précision et génère un nombre important de faux positifs.

La méthode statistique constitue un compromis intéressant : elle améliore la précision tout en conservant un coût de calcul raisonnable.

La méthode par graphe offre les meilleures performances en termes de détection, notamment pour identifier des comportements complexes. Cependant, elle nécessite davantage de ressources.

---

## Conclusion

Aucune méthode n’est optimale dans tous les cas.
Les méthodes simples sont plus sobres mais moins efficaces, tandis que les méthodes avancées sont plus performantes mais plus coûteuses.

L’objectif est donc de trouver un compromis entre sobriété, efficacité et précision.

