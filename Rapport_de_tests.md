# Rapport de tests - Vérin électrique TiMOTION TA16-5J-1

## 1. Objectif des essais

Des essais ont été réalisés sur le vérin électrique TiMOTION TA16-5J-1 afin de comprendre son fonctionnement, d'identifier ses connexions électriques et de déterminer les causes empêchant son extension.

Ces manipulations avaient également pour objectif de recueillir les informations nécessaires à la réalisation de la documentation technique du vérin.

Les essais ont porté sur l'identification du connecteur et des câbles, l'alimentation du moteur, les capteurs à effet Hall et l'inspection interne du vérin. À la suite des résultats obtenus, un second vérin a également été testé afin de comparer son fonctionnement avec celui du premier exemplaire.

## 2. Matériel utilisé

Les essais ont été réalisés à l'aide du matériel suivant :

- **Alimentation de laboratoire** : [nom et référence de l'alimentation à compléter].
- **Breadboard** : utilisée pour faciliter la réalisation des connexions électriques pendant les essais.
- **Fils Dupont mâle-mâle** : utilisés pour réaliser les liaisons électriques entre les différents éléments.
- **Bornier à vis 6 pôles** : utilisé pour raccorder et maintenir les conducteurs électriques grâce à des vis de serrage.
- **Multimètre** : utilisé pour identifier les conducteurs et effectuer les vérifications électriques.
- **Oscilloscope** : utilisé lors des tentatives d'observation des signaux des capteurs à effet Hall.

La prise d'origine du premier vérin a été coupée afin d'accéder aux conducteurs électriques et de faciliter leur identification et leur raccordement au matériel de test.

## 3. Préparation du câblage expérimental

Après avoir coupé la prise du vérin, les conducteurs ont été repérés à l'aide d'un multimètre afin d'identifier leurs couleurs et leur emplacement dans le connecteur.

Une breadboard, des fils Dupont mâle-mâle et un bornier à vis 6 pôles ont ensuite été utilisés pour réaliser les connexions nécessaires aux essais.

L'alimentation de laboratoire a servi à appliquer la tension de 24 V DC au moteur et à réaliser les essais d'alimentation. Elle a également été utilisée lors des tentatives d'alimentation des capteurs à effet Hall en 5 V DC.

Pour les essais à l'oscilloscope, un fil a été utilisé comme sonde de contact afin de tenter de relever les signaux présents sur les sorties des capteurs Hall.

## 4. Identification du connecteur et des câbles

### 4.1. Observation du connecteur

Dans un premier temps, la prise du vérin a été coupée afin d'observer les câbles présents et leur emplacement dans le connecteur.

Un multimètre a ensuite été utilisé pour identifier les conducteurs et faciliter le repérage des différentes connexions électriques.

Cette étape a permis de relever les couleurs des fils et leur position dans le connecteur, informations ensuite utilisées pour établir le tableau de câblage de la documentation technique.

### 4.2. Identification des connexions

Les différents fils ont été repérés afin de distinguer ceux associés à l'alimentation du moteur de ceux associés aux capteurs à effet Hall.

Les fonctions supposées des conducteurs ont ensuite été utilisées pour réaliser les premiers essais d'alimentation.

Les couleurs des fils, leur emplacement et les fonctions retenues sont présentés dans le fichier de documentation technique `verin-timotion.md`.

## 5. Essais d'alimentation du moteur

### 5.1. Première alimentation en 24 V DC

Une alimentation de 24 V DC a été appliquée au vérin afin de vérifier son fonctionnement et d'observer le mouvement de la tige.

Lors de ce premier essai, la tige du vérin s'est légèrement rétractée. Le moteur a donc produit un mouvement, mais le comportement observé ne permettait pas de confirmer le fonctionnement normal de l'actionneur.

### 5.2. Inversion de la polarité

La polarité de l'alimentation a ensuite été inversée afin de tenter de commander le mouvement dans le sens opposé.

Lors de cet essai, aucun mouvement n'a été observé. L'alimentation indiquait une tension de 24 V, mais un courant nul de 0 A.

Lorsque le branchement initial a été rétabli, l'alimentation s'est immédiatement mise en situation de court-circuit.

Ces observations ont montré un comportement électrique anormal du vérin. Les essais d'alimentation n'ont donc pas permis d'obtenir un fonctionnement normal dans les deux sens de déplacement.

**Remarque :** les observations réalisées ne permettent pas, à elles seules, d'identifier précisément l'origine du défaut électrique.

### 5.3. Mesure de la résistance des bornes du moteur

Une mesure de résistance a été réalisée à l'aide d'un multimètre entre les bornes du moteur du vérin, afin de vérifier la continuité électrique de l'enroulement.

Au lieu d'obtenir une valeur de résistance exprimée en ohms, le multimètre a affiché **OL** (*Over Limit* ou dépassement de plage, selon l'appareil).

Cette indication correspond généralement à une résistance trop élevée pour la plage de mesure sélectionnée ou à un circuit ouvert. Dans le cas présent, ce résultat est inhabituel pour une mesure réalisée directement aux bornes d'un moteur électrique et constitue un indice supplémentaire d'un éventuel défaut électrique.

Cependant, cette mesure ne permet pas à elle seule de conclure définitivement à une panne du moteur. Le résultat peut notamment dépendre des points de mesure, de la configuration du câblage et de la plage utilisée sur le multimètre.

## 6. Essais sur les capteurs à effet Hall

### 6.1. Alimentation des capteurs

L'hypothèse d'un problème lié aux capteurs à effet Hall a été envisagée pour tenter d'expliquer l'absence d'extension du vérin.

Une alimentation de 5 V DC a donc été appliquée aux connexions supposées correspondre à l'alimentation des capteurs Hall.

Cette manipulation n'a pas permis de rétablir le fonctionnement du vérin. Aucun mouvement supplémentaire permettant de confirmer cette hypothèse n'a été obtenu.

### 6.2. Observation des signaux à l'oscilloscope

Un oscilloscope a ensuite été utilisé dans le but d'observer les signaux de sortie des capteurs Hall.

Un fil a été utilisé comme sonde de contact pour tenter de relever les signaux sur les sorties des capteurs.

L'objectif était de vérifier la présence éventuelle d'impulsions électriques lors d'une tentative de déplacement du vérin.

Cependant, les essais n'ont pas permis d'obtenir de signaux exploitables. Il n'a donc pas été possible de confirmer le fonctionnement des capteurs Hall ni de déterminer si leur état avait un lien avec le défaut constaté.

## 7. Inspection interne et remplacement du vérin

### 7.1. Inspection interne du premier vérin

Afin de rechercher une éventuelle anomalie mécanique ou électrique, le moteur et l'intérieur du vérin ont été ouverts pour examiner les câbles et l'installation interne.

Cette inspection n'a pas permis d'identifier de défaut évident ni de relever d'information supplémentaire permettant d'expliquer précisément le dysfonctionnement.

L'origine de la panne n'a donc pas pu être déterminée par cette seule observation.

### 7.2. Essais sur le vérin de remplacement

À la suite des différents essais réalisés, le comportement du premier vérin restait difficile à comprendre. Malgré les tentatives d'alimentation en 24 V DC, les vérifications des capteurs à effet Hall et l'inspection interne, aucun fonctionnement normal n'avait pu être obtenu.

Le premier vérin a donc été remplacé par un second exemplaire afin de poursuivre les travaux.

Une alimentation de 24 V DC a alors été appliquée aux connexions du moteur du nouveau vérin. Contrairement au premier exemplaire, ce vérin a fonctionné et sa tige a pu se déplacer avec uniquement l'alimentation de 24 V DC, sans alimentation externe de 5 V DC appliquée aux capteurs à effet Hall.

Cet essai a permis de constater que l'application d'une alimentation externe de 5 V DC aux capteurs Hall n'était pas nécessaire pour obtenir le mouvement du moteur dans les conditions du test. Il faut toutefois distinguer le fonctionnement du moteur de celui des capteurs, qui peuvent servir à fournir un retour d'information sur le déplacement.

La comparaison des deux exemplaires a conduit à conclure que le premier vérin était très probablement défectueux. La cause exacte de cette défaillance n'a cependant pas pu être déterminée.

## 8. Bilan des essais

Les essais réalisés ont permis d'identifier les conducteurs, d'étudier le comportement électrique du premier vérin et de comparer son fonctionnement avec celui d'un second exemplaire.

| Essai réalisé | Observation | Conclusion |
|---|---|---|
| Identification des câbles au multimètre | Repérage des couleurs et de leur emplacement dans le connecteur | Informations utilisées pour la documentation technique |
| Alimentation du premier vérin en 24 V DC | Légère rétraction de la tige | Mouvement observé, fonctionnement normal non confirmé |
| Inversion de la polarité du premier vérin | Aucun mouvement et courant indiqué de 0 A | Fonctionnement anormal |
| Rétablissement du branchement initial | Mise en situation de court-circuit de l'alimentation | Défaut électrique suspecté |
| Mesure de la résistance aux bornes du moteur du premier vérin | Affichage `OL` sur le multimètre | Résultat compatible avec un circuit ouvert ou une résistance hors plage |
| Alimentation des capteurs Hall en 5 V DC | Aucun rétablissement du fonctionnement du premier vérin | Hypothèse non confirmée |
| Observation des signaux Hall à l'oscilloscope | Aucun signal exploitable obtenu | Fonctionnement des capteurs non vérifié |
| Inspection interne du premier vérin | Aucun défaut évident identifié | Origine de la panne non déterminée |
| Alimentation du second vérin en 24 V DC | Déplacement de la tige sans alimentation externe de 5 V DC appliquée aux capteurs Hall | Fonctionnement du moteur confirmé dans les conditions de l'essai |

## 9. Conclusion

Les essais réalisés ont permis de recueillir des informations sur les connexions électriques du vérin TiMOTION TA16-5J-1 et d'étudier plusieurs hypothèses pouvant expliquer le dysfonctionnement du premier exemplaire.

Les premières manipulations ont mis en évidence un comportement électrique anormal : mouvement limité de la tige, absence de déplacement lors de l'inversion de polarité, mise en situation de court-circuit de l'alimentation et affichage `OL` lors de la mesure de résistance aux bornes du moteur. Les essais sur les capteurs à effet Hall et l'inspection interne n'ont pas permis d'identifier précisément l'origine du problème.

Le remplacement du premier vérin par un second exemplaire a permis de poursuivre les essais et d'obtenir un déplacement de la tige avec uniquement une alimentation de 24 V DC sur le moteur, sans alimentation externe de 5 V DC appliquée aux capteurs Hall.

La comparaison des résultats a conduit à considérer le premier vérin comme défectueux. Toutefois, la cause exacte de sa panne n'a pas pu être déterminée.

Enfin, les observations recueillies au cours de ces manipulations ont servi de base à la rédaction de la documentation technique `verin-timotion.md`. Les résultats spécifiques au premier vérin doivent être distingués des caractéristiques qui pourront être confirmées sur le vérin de remplacement.
