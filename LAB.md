# Feuille de route du labo

Le labo explore ce qu’une petite infrastructure peut faire avec du matériel existant : répondre à partir de documents locaux, contrôler les outils qu’un modèle peut appeler et fonctionner quand Internet disparaît. Chaque piste ci-dessous a une question à trancher et une preuve à publier.

## Les trois prochains jalons

| Ordre | Question | Preuve attendue |
| --- | --- | --- |
| 1 · Le Phare sur machine de réemploi | Le registre survit-il à un redémarrage, réseau coupé ? | Même fichier avant et après redémarrage. Acceptation initiale, refus `replay` au second import, registre inchangé après le refus. [Protocole](https://github.com/log371/airgap-lab/blob/main/experiments/phare-bulletins/PROTOCOL-OFFLINE.md) |
| 2 · Banc d’IA locale | Quels compromis impose le matériel existant ? | Deux configurations sur la même tâche. Inventaire, versions, débit, latence, mémoire et, si un wattmètre est disponible, puissance à la prise. Publier les mesures brutes et le protocole. [Airgap Lab](https://github.com/log371/airgap-lab) |
| 3 · Pilote documentaire sur site | Une réponse peut-elle être retracée et comparée après un changement de modèle ? | Corpus fictif, réponses avec et sans source, deux exécutions comparables et rapport de régression. [SentinelIA](https://github.com/log371/sentinel1.2) · [LocalProof](https://github.com/log371/localproof) |

Le premier jalon est déjà reproductible entre deux processus en test automatisé. La preuve sur machine physique reste à produire. Le banc et le pilote documentaire sont des propositions de travail.

## Pistes à ouvrir après ces preuves

| Piste | Premier essai utile |
| --- | --- |
| **LoRa Mesh** | Comparer une liaison directe et une liaison avec relais à réglages fixes. Mesurer reçus uniques, pertes, doublons et délais avec des messages courts. Traiter ensuite la livraison du bulletin complet et sa vérification comme deux étapes séparées. [Banc proposé](https://github.com/log371/airgap-lab/blob/main/experiments/phare-bulletins/README.md#lora-mesh) |
| **Bulletins lus par une IA locale** | Utiliser des bulletins fictifs acceptés par Le Phare. Produire un résumé qui renvoie au texte original, puis comparer les sorties après changement de modèle. La signature authentifie le bulletin. Son texte reste une donnée à examiner. |
| **Permissions et mises à jour hors ligne** | Tester, sur un corpus fictif, un document lisible et un document interdit. Conserver la décision de politique, puis vérifier qu’un retour à une version signée précédente reste possible. [Skillbook](https://github.com/log371/Skillbook) · [SentinelIA](https://github.com/log371/sentinel1.2) |
| **Poste local accessible et Minitel** | Tester deux interactions simples, consulter un bulletin et le faire lire à voix haute. Observer d’abord la lisibilité et le clavier, puis décider si un terminal rétro est une interface pertinente. |
| **OpenTV** | Évaluer une navigation 1080p sur une TV existante, pilotée depuis l’iPhone. Mesurer le temps de reprise après redémarrage et séparer les médias locaux des services en ligne. |
| **Sobriété matérielle** | Comparer deux machines sur un service identique. Relever consommation au repos, pendant l’usage et temps de maintenance. Estimer l’impact d’un remplacement uniquement avec des hypothèses explicites. [Note sur le réemploi](https://julienl.dev/lab/valorisation) |

## Comment les projets peuvent se rejoindre

- **Qualifier le poste** avec Airgap Lab et le banc de mesures.
- **Recevoir une information** avec Le Phare et qualifier séparément son transport.
- **Chercher et citer** dans un corpus de test avec SentinelIA.
- **Limiter les actions d’un outil** et vérifier ses mises à jour avec Skillbook.
- **Comparer les résultats** avec LocalProof avant de changer un modèle ou une configuration.

Cette carte décrit des rôles complémentaires. Les raccordements entre dépôts restent à prototyper.

## Publier la preuve sur GitHub

Une expérience commence par une question dans le dépôt concerné. Un changement testable passe par une PR. Une version publiée indique ce qu’un autre poste peut rejouer et avec quels fichiers. Les résultats négatifs et les limites restent utiles s’ils sont documentés.

Pour chaque essai, consigner le commit, la machine, les versions, les commandes, le résultat attendu, le résultat observé et les traces partageables. Utiliser des données fictives pour les démonstrations.
