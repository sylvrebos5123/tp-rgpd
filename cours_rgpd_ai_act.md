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

### Chapitre 4

En vertu du principe de minimisation du RGPD (article 5), l'équipe ne doit surtout pas demander le dossier médical complet, mais uniquement les données strictement pertinentes pour prédire ou analyser une réhospitalisation.

Pour cette finalité précise, 5 catégories de colonnes suffisent généralement : identifiant pseudonymisé, délai entre les séjours, catégorie d'âge, diagnostic principal et comorbidités, type de sortie et durée de séjour.

La mission d'intérêt public (Article 6.1.e) : C'est la base privilégiée pour les hôpitaux (publics ou privés exerçant une mission de service public de soins) lorsqu'ils cherchent à améliorer la qualité des soins ou à mener des recherches scientifiques d'intérêt général.
L'intérêt légitime (Article 6.1.f) : Peut être invoqué par un établissement privé pour optimiser son organisation interne et réduire les réhospitalisations évitables, à condition que cela ne porte pas atteinte aux droits des patients.

2. La condition supplémentaire pour les données de santé (Article 9 du RGPD)
Par principe, le traitement des données de santé est interdit. Pour lever cette interdiction, il faut remplir au moins une exception de l'article 9.2, selon la finalité de l'étude :
 
Si l'étude vise à améliorer le suivi médical (rappel des patients) :
L'exception applicable est la prise en charge sanitaire et la gestion des systèmes et services de soins de santé (Article 9.2.h).
Condition supplémentaire stricte : Les données doivent obligatoirement être traitées par un professionnel de santé soumis au secret professionnel (ou sous sa responsabilité), conformément au droit belge (loi relative aux droits du patient).
Si l'étude est un projet de recherche scientifique ou statistique pur :
L'exception applicable est la recherche scientifique ou statistique (Article 9.2.j).
Condition supplémentaire stricte (Droit belge - Loi du 30 juillet 2018) : L'équipe doit mettre en place des garanties appropriées, notamment la pseudonymisation préalable des données (via un tiers de confiance ou un intermédiaire au sein de l'hôpital), tenir un registre précis des traitements, et soumettre le protocole à un comité d'éthique si la loi belge sur l'expérimentation humaine s'applique.

### Chapitre 5

Pour protéger la vie privée des patients et respecter le RGPD (notamment le principe de protection des données dès la conception / Privacy by Design et le secret médical), il faut cloisonner les rôles. Personne dans l'équipe ne doit avoir accès à l'ensemble des informations.

1. Data Manager
 
Dossiers bruts + Table de correspondance (Code ↔ Identité).
 
2. Data Scientists
 
Uniquement les colonnes minimisées et pseudonymisées (Code #482, tranche d'âge, diagnostic CIM-10, durée de séjour).
 
3. Équipe soignante
 
Identité du patient + Dossier médical complet + La recommandation de l'IA (uniquement pour les patients ciblés).

1. Le droit à exercer : Le droit de rectification
En vertu de l'article 16 du RGPD (et de la loi belge relative aux droits du patient), toute personne a le droit d'obtenir la correction des données inexactes la concernant dans les meilleurs délais (en principe sous un mois).
 
Nuance importante en milieu médical : Si l'erreur porte sur une donnée administrative (adresse, âge, date), elle est corrigée directement. Si le patient conteste un diagnostic médical, le médecin ne peut pas toujours effacer l'appréciation clinique initiale pour des raisons de traçabilité légale des soins ; dans ce cas, le droit de rectification prend la forme d'un ajout d'une déclaration complémentaire (ou note rectificative) versée au dossier médical pour consigner la remarque du patient.
Impact sur l'IA : L'hôpital doit également veiller à ce que la donnée corrigée soit mise à jour dans la base utilisée par l'IA, afin d'éviter que l'algorithme ne fasse une suggestion erronée.
 
2. Vers qui orienter le patient ?
L'équipe d'analyse ne doit jamais traiter directement cette demande (puisqu'elle n'a pas accès à l'identité réelle du patient ni au dossier source). Le patient doit être dirigé vers deux interlocuteurs officiels au sein de l'hôpital :
 
Le Délégué à la Protection des Données (DPO) de l'hôpital : C'est le point de contact légal obligatoire pour toute demande liée aux droits RGPD. Il enregistrera la demande, vérifiera l'identité du patient et s'assurera du respect du délai légal de réponse (1 mois).
Le médecin traitant hospitalier (ou le service de médiation / secrétariat médical) : C'est le seul habilité à valider et modifier le contenu clinique du dossier patient source (dossier patient informatisé - DPI).

### Chapitre 6

Au sein d'un même hôpital, ces deux outils relèvent de régimes radicalement différents :
 
1. L'IA répondant aux questions sur les horaires de visite : 
• Niveau de risque : Risque limité (obligations de transparence). Cet outil d'accueil administratif n'affecte ni les soins ni les droits fondamentaux des patients. Une erreur de réponse n'a pas d'impact critique sur la santé.
 
2. L'IA aidant à fixer l'ordre de passage aux urgences
 
• Niveau de risque : Haut risque. L'usage prévu consiste à hiérarchiser et prioriser l'accès aux soins d'urgence. Une défaillance, un biais ou une mauvaise évaluation peut entraîner un retard de prise en charge grave, voire mettre en danger la vie d'un patient.
 


