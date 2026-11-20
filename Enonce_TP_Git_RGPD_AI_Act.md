# TP — Construire un cours sur le RGPD et l'AI Act avec Git

## Situation

Un hôpital souhaite repérer les patients qui risquent d'être réhospitalisés pour leur proposer un appel de suivi. Vous rejoignez l'équipe chargée d'étudier ce projet. Avant d'utiliser les dossiers des patients ou de tester un outil d'intelligence artificielle (IA), elle veut comprendre ses responsabilités.

Votre mission consiste à **rédiger un cours** qui aide l'équipe à prendre ces décisions. Appuyez-vous sur vos recherches et enregistrez votre progression avec Git.

## Travail à réaliser

Créez un dépôt Git contenant un fichier `cours_rgpd_ai_act.md`. Rédigez les huit chapitres dans l'ordre indiqué et reprenez les titres et les messages de commit donnés ci-dessous.

Dans **chaque chapitre**, suivez ces consignes.

- Expliquez le sujet en vous appuyant sur une source fiable (texte officiel, autorité de protection des données ou publication institutionnelle).
- Ajoutez **une question ou un petit exercice** permettant à un lecteur de vérifier sa compréhension.
- Faites **un commit distinct** lorsque le chapitre est prêt.

Écrivez pour un camarade qui découvre le sujet. Les questions ci-dessous guident vos recherches. Vous pouvez reprendre le cas de l'hôpital ou choisir votre propre exemple.

## Chapitres à rechercher et à rédiger

### 1. Deux règlements pour deux questions

L'équipe veut d'abord analyser des dossiers, puis utiliser une IA pour suggérer qui rappeler. Quelle question le règlement général sur la protection des données (RGPD) invite-t-il à poser dès la première étape ? Quelle question le règlement européen sur l'IA (AI Act) ajoute-t-il à la seconde ?

Commit attendu — `docs: ajouter chapitre 1 - deux reglements`

### 2. Reconnaître une donnée personnelle

Dans un dossier fictif figurent un nom, un âge, une commune et un diagnostic. Quelles informations permettent de reconnaître une personne, seules ou par recoupement ? Qu'est-ce qui fait du diagnostic une donnée de santé ?

Commit attendu — `docs: ajouter chapitre 2 - donnees personnelles`

### 3. Pseudonymiser n'est pas anonymiser

L'hôpital remplace les noms par des codes et conserve la table de correspondance. Le fichier transmis à l'équipe est-il anonyme ? Cherchez ce qui permettrait encore de reconnaître un patient, même sans cette table. [Fiche de la CNIL sur l'anonymisation](https://www.cnil.fr/fr/technologies/lanonymisation-de-donnees-personnelles)

Commit attendu — `docs: ajouter chapitre 3 - anonymisation`

### 4. Définir un usage autorisé et proportionné

Pour étudier les réhospitalisations, l'équipe hésite à demander le dossier complet. Quelles colonnes lui sont réellement nécessaires ? Recherchez sur quelle base légale elle pourrait mener l'étude et quelle condition supplémentaire s'applique aux données de santé. [RGPD, articles 5, 6 et 9](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre2)

Commit attendu — `docs: ajouter chapitre 4 - usage des donnees`

### 5. Protéger les personnes et organiser le travail

Dans l'équipe, qui a besoin de voir quelles données et comment limiter les accès ? Un patient signale une erreur dans son dossier. Quel droit peut-il exercer et vers qui l'orienter ?

Commit attendu — `docs: ajouter chapitre 5 - protection`

### 6. Comprendre l'AI Act à partir des usages

Comparez deux IA d'un même hôpital. L'une répond aux questions sur les horaires de visite, l'autre aide à fixer l'ordre de passage des patients aux urgences. Comment l'usage prévu change-t-il le risque pour les personnes et les obligations à examiner ? [Présentation de l'AI Act par la Commission européenne](https://digital-strategy.ec.europa.eu/fr/policies/regulatory-framework-ai)

Commit attendu — `docs: ajouter chapitre 6 - ai act`

### 7. Évaluer une IA au-delà de sa performance globale

Sur 100 patients, 10 sont réhospitalisés. Un modèle qui prédit « aucune réhospitalisation » a donc raison 90 fois. Combien de patients à rappeler a-t-il repérés ? Cherchez un indicateur plus utile pour ce suivi et expliquez comment vérifier si le modèle manque davantage de patients dans une tranche d'âge.

Commit attendu — `docs: ajouter chapitre 7 - evaluation ia`

### 8. Appliquer les notions à un projet

L'hôpital envisage de tester l'IA pour choisir les patients à rappeler. Que lui conseillez-vous ? Appuyez votre décision sur les données que l'équipe peut utiliser et sur une vérification à faire avant de se fier aux prédictions. Précisez ce qu'il vous manque pour trancher, si nécessaire.

Commit attendu — `docs: ajouter chapitre 8 - cas pratique`

## Consignes Git

### 1. Initialiser le travail

Créez un dossier de projet, ouvrez un terminal dans ce dossier et initialisez un dépôt Git.

Créez ensuite le fichier `cours_rgpd_ai_act.md`, contenant le titre du document et le premier chapitre.

### 2. Enregistrer chaque chapitre

À la fin du premier chapitre, vérifiez les modifications, ajoutez le fichier et créez le commit avec le message indiqué.

Répétez la même démarche après chacun des sept chapitres suivants. Enregistrez chaque chapitre avant de commencer le suivant.

### 3. Contrôler l'historique

Affichez l'historique. Vous devez y retrouver **au moins huit commits**, correspondant aux huit chapitres.

## Illustration facultative

Vous pouvez ajouter un schéma original dans un dossier `illustrations/` lorsqu'il rend un concept plus compréhensible. Pensez à ajouter aussi l'image au commit correspondant. N'intégrez pas de captures contenant de véritables informations de patients.
