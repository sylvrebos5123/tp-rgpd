### Chapitre 1 
La transparence : Les personnes concernées ont-elles été informées que leurs données pouvaient être analysées de cette manière ?

Quel est le niveau de risque de ce système d'IA et quel degré de contrôle humain garantit-il ?

L'IA se contente-t-elle d'émettre une simple recommandation ou prend-elle une décision automatisée ?

### Chapitre 2
Dans ce dossier, toutes ces informations peuvent permettre d'identifier la personne, soit directement, soit indirectement par recoupement (c'est ce que le RGPD appelle la ré-identification)

Le nom (Identification directe) : Il permet à lui seul d'identifier l'individu immédiatement, sans information complémentaire.
L'âge, la commune et le diagnostic (Identification indirecte par recoupement) : Pris séparément, ces éléments semblent anonymes. Mais combinés entre eux, ils réduisent drastiquement le nombre de personnes correspondantes, jusqu'à n'en laisser qu'une seule (par exemple : une personne d'un âge précis, habitant une petite commune et souffrant d'une pathologie rare).

En vertu du RGPD, tant qu'un tel recoupement reste raisonnablement possible, le dossier n'est pas considéré comme anonyme mais comme pseudonymisé : il reste donc soumis à toutes les règles de protection des données (et notamment aux règles renforcées liées aux données de santé).

quelles seraient les méthodes pour anonymiser les données?

### Chapitre 3

Non, ce fichier n'est pas anonyme : il est pseudonymisé.
 
En vertu du RGPD (article 4), dès lors qu'une table de correspondance existe quelque part — même si elle est conservée uniquement par l'hôpital et que l'équipe n'y a pas accès — la ré-identification reste techniquement possible. Les données demeurent donc des données à caractère personnel.

1. L'individualisation (ou isolement)
Si une combinaison de données ne correspond qu'à un seul dossier dans le fichier, il est possible d'isoler cette personne sans même connaître son nom au départ.

2. La corrélation (croisement avec des sources externes)
Il est possible de croiser les attributs restants (âge, commune, diagnostic, ou d'éventuelles dates de passage) avec d'autres informations publiques ou accessibles à l'équipe

Par exemple, les réseaux sociaux, l'entourage, les collègues ou encore d'autres bases de données.

3. L'inférence (déduction)
Même sans certitude absolue, l'analyse des données permet de déduire avec une quasi-certitude qu'un dossier appartient à une personne connue, ou de deviner de nouvelles informations sur elle (par exemple, déduire l'identité d'un patient à partir de la fréquence de ses consultations ou de la rareté d'un traitement prescrit).

Comment pourrait-on neutraliser ces trois risques?


