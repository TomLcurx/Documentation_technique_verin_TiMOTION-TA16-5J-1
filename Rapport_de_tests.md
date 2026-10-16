# Rapport de tests — Vérin électrique TiMOTION TA16-5J-1

## 1. Objectif des essais

Des essais ont été réalisés sur le vérin électrique TiMOTION TA16-5J-1 afin de comprendre son fonctionnement, d'identifier ses connexions électriques et de déterminer les causes empêchant son extension.

Ces manipulations avaient également pour objectif de recueillir les informations nécessaires à la réalisation de la documentation technique du vérin.

Les essais ont porté sur l'identification du connecteur et des câbles, l'alimentation du moteur, les capteurs à effet Hall et l'inspection interne du vérin.

## 2. Identification du connecteur et des câbles

### 2.1. Observation du connecteur

Dans un premier temps, la prise du vérin a été coupée afin d'observer les câbles présents et leur emplacement dans le connecteur.

Un multimètre a ensuite été utilisé pour identifier les conducteurs et faciliter le repérage des différentes connexions électriques.

Cette étape a permis de relever les couleurs des fils et leur position dans le connecteur, informations ensuite utilisées pour établir le tableau de câblage de la documentation technique.

### 2.2. Identification des connexions

Les différents fils ont été repérés afin de distinguer ceux associés à l'alimentation du moteur de ceux associés aux capteurs à effet Hall.

Les fonctions supposées des conducteurs ont ensuite été utilisées pour réaliser les premiers essais d'alimentation.

Les couleurs des fils, leur emplacement et les fonctions retenues sont présentés dans le fichier de documentation technique `verin-timotion.md`.

## 3. Essais d'alimentation du moteur

### 3.1. Première alimentation en 24 V DC

Une alimentation de 24 V DC a été appliquée au vérin afin de vérifier son fonctionnement et d'observer le mouvement de la tige.

Lors de ce premier essai, la tige du vérin s'est légèrement rétractée. Le moteur a donc produit un mouvement, mais le comportement observé ne permettait pas de confirmer le fonctionnement normal de l'actionneur.

### 3.2. Inversion de la polarité

La polarité de l'alimentation a ensuite été inversée afin de tenter de commander le mouvement dans le sens opposé.

Lors de cet essai, aucun mouvement n'a été observé. L'alimentation indiquait une tension de 24 V, mais un courant nul de 0 A.

Lorsque le branchement initial a été rétabli, l'alimentation s'est immédiatement mise en situation de court-circuit.

Ces observations ont montré un comportement électrique anormal du vérin. Les essais d'alimentation n'ont donc pas permis d'obtenir un fonctionnement normal dans les deux sens de déplacement.

**Remarque :** les observations réalisées ne permettent pas, à elles seules, d'identifier précisément l'origine du défaut électrique.

## 4. Essais sur les capteurs à effet Hall

### 4.1. Alimentation des capteurs

L'hypothèse d'un problème lié aux capteurs à effet Hall a été envisagée pour tenter d'expliquer l'absence d'extension du vérin.

Une alimentation de 5 V DC a donc été appliquée aux connexions supposées correspondre à l'alimentation des capteurs Hall.

Cette manipulation n'a pas permis de rétablir le fonctionnement du vérin. Aucun mouvement supplémentaire permettant de confirmer cette hypothèse n'a été obtenu.

### 4.2. Observation des signaux à l'oscilloscope

Un oscilloscope a ensuite été utilisé dans le but d'observer les signaux de sortie des capteurs Hall.

L'objectif était de vérifier la présence éventuelle d'impulsions électriques lors d'une tentative de déplacement du vérin.

Cependant, les essais n'ont pas permis d'obtenir de signaux exploitables. Il n'a donc pas été possible de confirmer le fonctionnement des capteurs Hall ni de déterminer si leur état avait un lien avec le défaut constaté.

## 5. Inspection interne du vérin

Afin de rechercher une éventuelle anomalie mécanique ou électrique, le moteur et l'intérieur du vérin ont été ouverts pour examiner les câbles et l'installation interne.

Cette inspection n'a pas permis d'identifier de défaut évident ni de relever d'information supplémentaire permettant d'expliquer précisément le dysfonctionnement.

L'origine de la panne n'a donc pas pu être déterminée par cette seule observation.

## 6. Bilan des essais

Les essais réalisés ont permis de recueillir plusieurs informations sur le vérin, mais n'ont pas permis de rétablir son fonctionnement.

| Essai réalisé | Observation | Conclusion |
|---|---|---|
| Identification des câbles au multimètre | Repérage des couleurs et de leur emplacement dans le connecteur | Informations utilisées pour la documentation technique |
| Alimentation en 24 V DC | Légère rétraction de la tige | Mouvement observé, fonctionnement normal non confirmé |
| Inversion de la polarité | Aucun mouvement et courant indiqué de 0 A | Fonctionnement anormal |
| Rétablissement du branchement initial | Mise en situation de court-circuit de l'alimentation | Défaut électrique suspecté |
| Alimentation des capteurs Hall en 5 V DC | Aucun rétablissement du fonctionnement | Hypothèse non confirmée |
| Observation à l'oscilloscope | Aucun signal exploitable obtenu | Fonctionnement des capteurs non vérifié |
| Inspection interne | Aucun défaut évident identifié | Origine de la panne non déterminée |

## 7. Conclusion et remplacement du vérin

Les différentes manipulations n'ont pas permis de faire fonctionner normalement le vérin testé. Malgré les essais d'alimentation, les vérifications des capteurs à effet Hall et l'inspection interne, l'origine exacte du dysfonctionnement n'a pas pu être identifiée.

Le comportement électrique observé, notamment la mise en situation de court-circuit de l'alimentation, ainsi que l'impossibilité d'obtenir un déplacement normal, ont conduit à considérer le vérin comme hors service pour les besoins du projet.

Il a donc été remplacé par un autre vérin afin de poursuivre les travaux.

Les essais ont néanmoins permis d'identifier les connexions visibles, de relever certaines caractéristiques pratiques et de documenter les manipulations réalisées. Ces informations ont servi de base à la rédaction du fichier `verin-timotion.md`.

Il convient toutefois de distinguer les caractéristiques relevées sur le vérin initial des résultats qui devront éventuellement être confirmés sur le vérin de remplacement.

