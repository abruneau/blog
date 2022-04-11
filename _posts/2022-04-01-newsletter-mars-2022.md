---
layout: post
title: Newsletter Datadog France Mars 2022
tags: datadog newsletter
---

Bonjour à tous,

Suite à de nombreuses demandes, voici la première édition de notre newsletter Datadog. Chaque mois, recevez une synthèse des nouveautés et des évènements à venir.

- [Événements passés et futurs](#événements-passés-et-futurs)
- [Les nouveautés du mois](#les-nouveautés-du-mois)
  - [Intégrations](#intégrations)
    - [Pingdom](#pingdom)
    - [Dell EMC](#dell-emc)
  - [RUM](#rum)
    - [Browser Dev Tools](#browser-dev-tools)
    - [Unified Query Editor](#unified-query-editor)
    - [Vues Enregistrées](#vues-enregistrées)
    - [Moniteur RUM](#moniteur-rum)
  - [Synthetics](#synthetics)
    - [gRPC api test](#grpc-api-test)
    - [Injecter le SDK RUM dans tous les tests de navigateur synthétique](#injecter-le-sdk-rum-dans-tous-les-tests-de-navigateur-synthétique)
  - [APM](#apm)
    - [Serverless Monitoring](#serverless-monitoring)
  - [Log Management](#log-management)
    - [Surveillez l'utilisation des Log](#surveillez-lutilisation-des-log)
    - [Détection d'anomalies en temps réel](#détection-danomalies-en-temps-réel)
    - [Ajoutez des filtres d'exclusion directement à partir des patterns](#ajoutez-des-filtres-dexclusion-directement-à-partir-des-patterns)
  - [Sécurité](#sécurité)
    - [CSPM et Azure](#cspm-et-azure)
    - [Détection de voyages impossibles de Cloud SIEM](#détection-de-voyages-impossibles-de-cloud-siem)
    - [Contrôlez qui peut modifier vos moniteurs avec Monitors RBAC](#contrôlez-qui-peut-modifier-vos-moniteurs-avec-monitors-rbac)
    - [Évaluez l'exposition des données sensibles](#évaluez-lexposition-des-données-sensibles)

# Événements passés et futurs

Si n’aviez pas pu assister au webinaire sur notre offre sécurité de février, vous pouvez consulter le replay [sur notre](https://www.datadoghq.com/fr/dg/webinars/security-fr/) site.

En avril, vous pourrez nous retrouver à deux occasions :

- Le 12 avril à l'AWS Summit où nous serons présents. Vous pouvez vous inscrire à l'adresse suivante et nous retrouver sur place sur notre stand : <https://pages.awscloud.com/partner-paris-summit-2022.html>
- Le 14 avril pour un webinaire autour de l'UX monitoring et de session replay. Vous pouvez vous inscrire à l'adresse suivante : <https://www.datadoghq.com/fr/dg/webinars/ux-webinar-fr/>

# Les nouveautés du mois

## Intégrations

### Pingdom

La mise à jour de l'[intégration Pingdom](https://app.datadoghq.eu/account/settings#integrations/pingdom-v3) vous permet de facilement intégrer votre compte Pingdom à l'aide de l'[API V3.1](https://docs.pingdom.com/api/), qui prend en charge OAuth pour une expérience de surveillance plus sécurisée. L'intégration Pingdom vous permet de suivre la disponibilité, les temps d'arrêt et les performances de vos sites Web dans Datadog.

L'antienne intégration de l'API Pingdom utilise l'[API V2.1](https://docs.pingdom.com/api/), qui s'appuie sur l'authentification de base. Cette version de l'API est depuis obsolète et n'est plus prise en charge par Pingdom. Si vous utilisez l'ancienne intégration de l'API Pingdom, nous vous encourageons vivement à passer à la nouvelle version, qui possède la même télémétrie - avec des avantages supplémentaires en matière de sécurité et de stabilité.

### Dell EMC

Nous sommes heureux d'annoncer que vous pouvez surveiller vos clusters Dell EMC Isilon avec une nouvelle offre d'intégration de Crest Data Systems, qui est maintenant disponible sur la marketplace Datadog. Cette nouvelle offre s'appuie sur les métriques liées au matériel et aux processus proposées par le produit Network Device Monitoring de Datadog, et fournit un aperçu plus approfondi des métriques entourant le système de fichiers, la mise en cache, les performances et d'autres domaines.

Cette nouvelle offre propose cinq tableaux de bord prêts à l'emploi qui offrent une plongée approfondie dans la santé et le fonctionnement de vos clusters et nœuds Dell EMC Isilon. Vous pouvez désormais suivre les métriques de débit et d'utilisation du pool de nœuds, voire des informations sur les événements Isilon, analyser les taux d'accès au cache, etc., ainsi que les données du reste de votre pile technologique dans Datadog. Pour tester cette intégration gratuitement pendant 14 jours, visitez la vignette d'intégration Dell EMC Isilon de Crest Data Systems sur la marketplace Datadog, qui se trouve dans l'application Datadog sous « Intégrations » > « Marketplace ».

Pour plus de détails, vous pouvez consulter notre [documentation](https://docs.datadoghq.com/integrations/crest_data_systems_dell_emc_isilon/), ainsi que le [blog](https://www.datadoghq.com/blog/dell-emc-isilon-monitoring-crest-data-systems-datadog-marketplace/) Crest Data Systems Dell EMC Isilon de Datadog.

## RUM

### Browser Dev Tools

Nous sommes ravis d'annoncer que Session Replay Browser Dev Tools est désormais disponible en version bêta. Session Replay est une reproduction de type vidéo de l'expérience d'un utilisateur lors de la navigation sur votre site Web. Elle vous permet de voir exactement comment vos utilisateurs interagissent avec vos applications web, ce qui vous permet d'économiser du temps dans la reproduction du comportement de votre utilisateur.

Browser Dev Tools est un nouveau mode de lecture intégré directement dans l'interface Session Replay qui vous permet de déboguer et d'identifier la cause première des problèmes encore plus rapidement :

- Expose des informations clés sur une session de lecture, telles que la cascade détaillant les goulots d'étranglement des performances
- Met en évidence les erreurs qui se produisent juste après une action de l'utilisateur et met même en évidence les erreurs qui sont un problème courant dans votre application
- Lecture d'une chronologie des journaux du navigateur de la session pendant que l'enregistrement est en cours.

![](https://lh5.googleusercontent.com/UHJkZtfq1mk6y1S2ug_BxlsEwB5duRgG_ttpfYPMxTsA4uJBbHjXEXr_4JBudax_3NnnHxDL9sUiRWT-TK2vtvw7AKaM4NLTiw7VmYtgWTszVP-n66NRVMBsZArzuP-fawuhlxAW)

Browser Dev Tools est désormais disponible pour tout le monde en version bêta sur le produit Session Replay en cliquant sur le bouton [</> Dev Tools] dans l'en-tête Session Replay.

### Unified Query Editor

Nous sommes ravis d'annoncer que nos précédentes expériences RUM Search et RUM Analytics ont été combinées dans un seul éditeur de requêtes unifié. Sans aucune configuration supplémentaire, vous pouvez désormais basculer entre les workflows suivants sans changer d'écran :

- trouver des sessions utilisateur, des pages vues, des appels réseau ou des erreurs qui remplissent un critère donné
- visualiser les données par navigateur, pays ou tout autre attribut, que ce soit OOTB ou personnalisé
- créer des entonnoirs d'expérience utilisateur pour comprendre la conversion tout au long des parcours utilisateur critiques dans votre application

[Essayer maintenant](https://app.datadoghq.eu/rum/explorer?tab=session&from_ts=1641887658482&to_ts=1641891258482&live=true) ou [découvrez en plus dans notre documentation](https://docs.datadoghq.com/real_user_monitoring/explorer/?tab=facets). ![](https://lh4.googleusercontent.com/ibRfOdQBf_DXWPHJ5-l3k0s1f8jOb6Uko8vsfpoKvYnJ6wdtIgJ_FoBdKK3TwXQbjEerWOgWMOeGTUGMjhvdePsS4CnsmV8rJrMiZ7TZS0gGNfqQrQ9ZuUk9vpWDz7KnFATC6sUg)

### Vues Enregistrées

Nous sommes ravis d'annoncer que vous pouvez désormais facilement enregistrer, personnaliser et partager vos recherches dans RUM grâce aux vues enregistrées ! Cette version permet également à RUM d'avoir

- des vues enregistrées prédéfinies offrant des vues enregistrées personnalisées et prêtes à l'emploi créées par Datadog
- Masquer/afficher les facettes offrant la possibilité d'étendre la liste des facettes pour afficher les facettes pertinentes

Avec l'ajout de vues enregistrées dans RUM, les utilisateurs peuvent désormais

- Enregistrer leur état de requête de recherche, facettes, visualisation (toplist, funnel, geomap…)
- Afficher, personnaliser et partager leurs vues enregistrées pour un dépannage collaboratif
- Personnaliser et contrôler complètement leur vue par défaut de l'explorateur/des analyses
- Obtenir des suggestions de saisie semi-automatique dans la barre de recherche pour les vues enregistrées

![](https://lh3.googleusercontent.com/-9lFKSHaCOYkaRaS_W93t9olSBI15TGSKqFkyWGEOlCOP2Qa7f-cxvHrQC8o6_8MKep2ZWPNQxHPC33M9xwWBT1Hr0VmOYpWI2crvZv_GQYF5sExAAOkH5bD6r8kxPiOVoRxLshT)

De plus, Datadog RUM ajoute automatiquement des vues enregistrées prédéfinies pour vos cas d'utilisation les plus courants afin de vous aider à lancer un dépannage efficace.

En savoir plus sur la fonctionnalité dans la [documentation](https://docs.datadoghq.com/real_user_monitoring/explorer/saved_views/).

### Moniteur RUM

Les moniteurs RUM prennent désormais en charge l'ajout de formules et de fonctions.

- Formules : combiner plusieurs requêtes en un seul moniteur en ajoutant des mathématiques pour les enchaîner
- Fonctions : La possibilité d'appliquer une fonction à une requête comme le max, le timeshift ou le lissage par exemple.

Au lieu de vous fier à des seuils d'alerte prédéfinis, vous pouvez désormais configurer des moniteurs RUM pour qu'ils alertent si le trafic est inférieur de plus de 20 % à la semaine précédente et identifier les problèmes tout en coupant les modèles de fluctuation de l'heure du jour/de la semaine dans le trafic des utilisateurs. D'autres exemples de cas d'utilisation incluent le déclenchement de notifications basées sur :

- Le pourcentage de sessions sans plantage
- Le revenu moyen généré par un groupe de clients est nettement inférieur au revenu généré par d'autres groupes.

![](https://lh6.googleusercontent.com/JaCPD3XtbL258xc7AJiWRFgO7kTmfcQ0ln_L9dmBhcqoxHl54gAhszQVoEfEHFMZIrBIdyhiT6w6y_4xuczaC4WxWQrQfKaKD6KBKmhqIsY4lqUWcjKGEs232taZRteaKMpvYNtR)

## Synthetics

### gRPC api test

Ce nouveau type de test vous permet d'envoyer des vérifications de l'état du service gRPC. [La vérification de l'état gRPC](https://github.com/grpc/grpc/blob/master/doc/health-checking.html) est une norme pour signaler l'état des services gRPC. Il vous permet de déterminer si vos serveurs et services gRPC sont réactifs, en cours d'exécution et capables de répondre aux demandes. ![](https://lh5.googleusercontent.com/LUyzpDmUjOT0CN6zEOo8MdLb4D-W6Pmjb_WrQ-5a8BLATedgU3lEeEU28Xx7tmMxcQssFHK-rJ28jmHMLBeZgIFoJp166FcXQfcPKlllTfJ44PTlG2Gd3VoTfvHrh7QAkQ8K8ebU)

Consultez notre [documentation](https://docs.datadoghq.com/synthetics/api_tests/grpc_tests) pour en savoir plus sur gRPC

### Injecter le SDK RUM dans tous les tests de navigateur synthétique

Vous avez maintenant la possibilité d'injecter le SDK RUM dans tous les tests de navigateur synthétique. Cela signifie que vous pourrez utiliser les fonctionnalités RUM (Session Replay, Error Tracking…) sur les applications où vous ne pouvez pas installer RUM, et sur toutes vos sessions générées par Synthetic. ![](https://lh6.googleusercontent.com/RJu1xQF-oF4Voa9kiIXVXgm2u5wzKqOG7J61il8hu8obNNF-y0CcKJTPXJkhWVsdECvH2dT29i06_GiGL7ECGo3Y9nL3A3SNuPgh_94jcYHN5sJzPLVK-xi4zyJbIByr-Kln-cFS)

![](https://lh3.googleusercontent.com/1pBKp2G4wZX4ZqhB5TnY_gxjnyCTu_2nD2VGGfp8qdrb_fgKiYLKyim4laNDqlllEFNS1PJXYTTTAb2kdp46XQ9yXMq65pvoMuZdFDURR9xx3jex3mb3jmDru0hi_0nsSDQiICZ_)

L'injection du SDK RUM dans les tests du navigateur Synthetics débloque :

1. Session Replays pour toutes les exécutions de test. Ils fournissent plus de contexte que les captures d'écran déjà disponibles pour chaque étape. Avec cette fonctionnalité, vous disposez désormais de l'enregistrement et des outils de développement associés (bêta) pour vous aider à comprendre la cause première des échecs de test.
2. La collecte et le regroupement des erreurs des tests navigateur dans Error Tracking. Vous permettant d'être alerté si un nouveau problème apparaît, de comprendre son ampleur, la version qui l'a introduite et d'obtenir la ligne de code qui a déclenché l'erreur.
3. La collecte de données RUM sur les applications dont vous ne pouvez pas accéder au code source et installer le SDK.
4. RUM surveille et interroge vos tests synthétiques. Cela vous permet de créer des tableaux de bord et des alertes personnalisés. Par exemple, vous pouvez être alerté si une ressource volumineuse prend trop de temps à charger.

Lisez notre [guide](https://docs.datadoghq.com/synthetics/guide/explore-rum-through-synthetics/) pour plus d'informations.

## APM

### Serverless Monitoring

Datadog Serverless fournit désormais un traçage APM amélioré dans les applications serverless avec AWS API Gateway, SQS, SNS, Kinesis et plus encore, vous permettant de surveiller facilement les dépendances de service et de réduire la latence afin que vos utilisateurs bénéficient de la meilleure expérience possible. <https://dtdg.co/3BgoGvh>

![](https://lh5.googleusercontent.com/AKCm4-Iq5kZugAlu3YC-f7FtY7lzSxV6CuQpgSfE-XvBrGh81ljjLLRcjiDZftRKjmo2wFZlcVSCWdPsFLhDfcai1Dwb3siGX2MAoEBLAt8m0XjJFzNID3j9M6bpsEP2aNOpS4B_)

Découvrez notre [documentation](https://docs.datadoghq.com/serverless/) et notre [récent billet](https://www.datadoghq.com/blog/tag/serverless-monitoring/) pour en apprendre plus sur Datadog Serverless Monitoring.

## Log Management

### Surveillez l'utilisation des Log

Log management propose dorénavant un [tableau de bord prêt à l'emploi](https://app.datadoghq.com/dash/integration/logs_estimated_usage) pour vous aider à surveiller l'utilisation des logs dans votre organisation. Analysez les statistiques liées à vos volumes d'ingestion de journaux, au débit du pipeline et à l'échantillonnage d'index pour obtenir une image complète de votre utilisation. Consultez notre [guide](https://docs.datadoghq.com/logs/guide/logs-monitors-on-volumes/) complet sur la surveillance de l'utilisation de Log Management pour en savoir plus.

![](https://lh4.googleusercontent.com/zxHmSULnRdepmudOLy4YLLVcaSAiOyiLl6T7bANU203ugJMbgGnrsG1PaXtsEjAEmoPb078sak7YIhmmu_N3fMVDcwP0BxsW3HoxwqXerWJLj2SKBISekNLzTUZmgJIpZqgu7kzE)

### Détection d'anomalies en temps réel

Datadog Log Management prend désormais en charge la détection d'anomalies en temps réel sur l'intégralité de votre flux de logs. Ce nouveau service analyse automatiquement tous vos logs entrant dans Datadog pour identifier des modèles inhabituels et détecter des problèmes qui auraient été auparavant difficiles à trouver. Les anomalies pertinentes sont mises en évidence dans Watchdog Insights, la fonctionnalité de corrélation et de recommandation de temps de requête de Watchdog, pour augmenter votre dépannage lors d'enquêtes critiques.

En fonction de votre requête, vous pouvez maintenant voir des informations intéressantes dans l'explorateur de journaux, telles que :

- L'émergence ou la modification des modèles de journalisation autour de différents services et statuts.
- Les comportements aberrants pour les journaux avec des messages d'erreur.
- Si cette tendance se poursuit ou non avec les journaux récents.
- Une vue détaillée des logs avec ces paternes et des valeurs aberrantes d'erreur.
- Une option en 1 clic pour affiner vos requêtes et partager ces informations avec votre équipe.

Log Anomaly Detection est disponible pour tous les utilisateurs de Datadog. [Essayez-le maintenant dans l'explorateur de logs](https://app.datadoghq.com/logs?query=&index=%2A&from_ts=1647456761403&to_ts=1647471161403&live=false)

![](https://lh3.googleusercontent.com/es-uUaJcMAgsS0Lu-w2bBqPBdaLfJrMb1nUiUrEGux3N6BroD53cA0wFqjZj_45QFJI4pjIQPoy3EB_3AteJ_AVnAd9jt6zWvD8pk87TnZyXPhf51VyS2qfxfAdzk16JQbqnIWPw)

Pour en savoir plus, consultez notre [documentation](https://docs.datadoghq.com/logs/explorer/watchdog_insights/).

### Ajoutez des filtres d'exclusion directement à partir des patterns

Ajoutez des filtres d'exclusion directement à partir de Log Patterns en un clic, ce qui vous évite d'avoir à copier des requêtes et à accéder à la page de configuration des logs. Ceci est particulièrement utile lors de pics de log lorsque vous souhaitez gérer rapidement vos volumes d'indexation pour respecter votre budget.

Consultez notre [documentation](https://docs.datadoghq.com/logs/guide/getting-started-lwl/#3-create-a-log-pattern-exclusion-filter) pour en savoir plus sur ces fonctionnalités et [commencez à l'utiliser dès aujourd'hui](https://app.datadoghq.com/logs?viz=pattern&agg_q=status%2Cservice).

## Sécurité

### CSPM et Azure

Cloud Security Posture Management analyse et détecte désormais les erreurs de configuration des principales ressources Azure telles que les services d'application, les comptes de stockage et les groupes de sécurité réseau. Cela vous permet de sécuriser vos actifs cloud et de suivre votre état de conformité, en fonction des exigences des cadres de conformité standard de l'industrie : PCI DSS, SOC 2, HIPAA, GDPR et CIS.

Préparez votre premier rapport de conformité en quelques minutes en activant CSPM pour vos abonnements Azure via [la vignette d'intégration Azure](https://app.datadoghq.eu/account/settings#integrations/azure) ou via la [page de configuration CSPM](https://app.datadoghq.eu/security/configuration?detect-threats=apache&secure-cloud-environment=azure&secure-hosts-and-containers=kubernetes&selected-products=compliance_monitoring). Vous pouvez également en savoir plus sur cette nouvelle fonctionnalité dans notre [article de blog dédié](https://www.datadoghq.com/blog/cspm-for-azure-with-datadog/).

Détections de Voyage Impossibles

L'équipe Cloud SIEM est heureuse d'annoncer que nous avons publié une toute nouvelle méthode de détection appelée "Impossible Travel".

Vous pouvez désormais identifier les informations d'identification d'utilisateurs compromises en identifiant le moment où le compte est vu à plusieurs endroits dans un laps de temps incroyablement court. ![](https://lh5.googleusercontent.com/CbKICq3Dq2V2HNNiH8fe7bjulnzzD4mVxTVpS4KbrWEVSE2iEJAoD07nExs6yr1FPvc5XsuMNpti1rs0oIphVDpFq3aSkx0eDl0O899XyV_d3rWmPem3TjNLTuNWoiOxwq8Xw3Oz)

Consultez notre [documentation](https://docs.datadoghq.com/security_platform/cloud_siem/log_detection_rules/?tab=threshold) pour en savoir plus sur la création et la gestion des détections de voyage impossibles !

### Détection de voyages impossibles de Cloud SIEM

![](https://lh6.googleusercontent.com/7DCz1dp1GuMU0EeLQQZeqAxASIxRHQgmHon32OE47laV-ZDObkygYFyrjbAd8nMEwvf0VSsf9T8cI-zkJ80TKdSRQbM2HoywalMgnVanrVTvTlUHFbo8k-cI41jW_vo9R_7skCqu)

Le nombre d'atteintes à la sécurité est en augmentation en raison d'informations d'identification compromises. Un utilisateur légitime peut utiliser son compte à New York. Pendant ce temps, un attaquant peut utiliser le même compte depuis Los Angeles. Datadog Cloud SIEM peut désormais détecter cela en inspectant l'emplacement et le moment des demandes d'un utilisateur et en déterminant si les emplacements sont suspects. Datadog réduit le nombre de faux positifs de ces signaux en apprenant où un utilisateur accède généralement à vos applications.

Avec cette nouvelle méthode de détection, 5 nouvelles règles de détection prêtes à l'emploi sont publiées en se concentrant sur les environnements AWS. Commencez à utiliser Impossible Travel en accédant à l'onglet [Règles de détection](https://app.datadoghq.eu/security/configuration/rules/new?product=siem) !

Consultez notre [documentation](https://docs.datadoghq.com/security_platform/cloud_siem/log_detection_rules/?tab=threshold) pour en savoir plus sur la création et la gestion des détections de voyage impossibles !

### Contrôlez qui peut modifier vos moniteurs avec Monitors RBAC

Les moniteurs garantissent que vos équipes sont alertées en cas de problèmes sur vos systèmes. S'assurer que seul le bon sous-ensemble d'utilisateurs peut modifier le bon sous-ensemble de moniteurs est essentiel pour éviter des changements accidentels dans les configurations de vos moniteurs. Vous pouvez désormais gérer vos moniteurs de manière plus sécurisée en limitant les autorisations de modification de chaque moniteur individuel à certains rôles spécifiques de votre compte :

![](https://lh6.googleusercontent.com/42O_5st_Cm6EWyGcqB04vPAIU07ydQmoWD6RnLJT4WAZbTxsP93rRtNZI6waQhNFjo8NwU8YIBLz0ggKpi-oDTLHU70mXG4i45Hiu0Up3dTezHcqG5BBv44KGwNpNk8FvfNzZnyh)

Consultez la documentation dès aujourd'hui pour savoir comment restreindre les autorisations de modification des moniteurs [via l'interface utilisateur](https://docs.datadoghq.com/monitors/notify/#permissions) et [via l'API](<https://docs>. [datadoghq.com/api/latest/monitors/#create-a-monitor](http://datadoghq.com/api/latest/monitors/#create-a-monitor)).

### Évaluez l'exposition des données sensibles

Sensitive Data Scanner propose désormais un [tableau de bord prêt à l'emploi](http://app.datadoghq.com/dash/integration/sensitive_data_scanner) pour vous aider à évaluer rapidement l'exposition de vos données sensibles, plus de 50 [règles d'analyse](https://app.datadoghq.com/organization-settings/sensitive-data-scanner/library) pour étendre votre visibilité, et des capacités de clonage et de filtrage pour accélérer [la création de groupes et de règles d'analyse](https://docs.datadoghq.com/account_management/org_settings/sensitive_data_detection). Consultez notre [article de blog](https://www.datadoghq.com/blog/sensitive-data-scanner/) ou la [documentation](https://docs.datadoghq.com/account_management/org_settings/sensitive_data_detection) pour en savoir plus sur le scanner de données sensibles.

![](https://lh5.googleusercontent.com/DEgnzNmbV6Qn4_Yb9k8IlLcP7KvSjVb5dPfFc_ehaHQu07fLjgezdITh-kbECu31x3mzD6icSdczB6qm-d_xQJrgUp3ffjOEiv_s8ko1fuEE9yhlqgNYjPfZfocrSYyysDQh8JHL)
