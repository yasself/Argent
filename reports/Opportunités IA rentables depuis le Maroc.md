# Opportunités IA depuis le Maroc : miser sur la veille B2B spécialisée

**Phase 1 — Intelligence d'opportunités et sélection stratégique. Rapport de recherche du 11 novembre 2026. Rien n'a été lancé : aucun client contacté, aucun compte ouvert, aucune dépense engagée, aucun test de demande exécuté.**

La réponse courte : le seul endroit où les agents IA, la contrainte « pas d'opérateur quotidien, pas d'appels de vente » et les rails de paiement marocains convergent est un petit portefeuille de **produits de veille B2B sur données publiques** (appels d'offres santé financés par les bailleurs en Afrique et dans l'UE, veille réglementaire cosmétiques/compléments alimentaires), vendus entre 45 et 150 USD par mois via un marchand officiel (merchant of record), complété par des scrapers publiés sur une place de marché (Apify) comme billet de loterie à coût quasi nul. Sur 80 modèles distincts recensés, 5 sont retenus, 32 restent conditionnels et 43 sont éliminés. Le profit attendu est **modeste** : la médiane des startups qui déclarent un revenu vérifié se situe autour de 145 USD de revenu mensuel récurrent, et nos scénarios centraux donnent environ 600 à 900 USD de résultat d'exploitation mensuel par produit d'abonnement au douzième mois, hors coût de structure et avant impôt, avec un scénario prudent proche de zéro. **Aucune source ne documente une entreprise entièrement autonome** : les expériences d'Anthropic et d'Andon Labs montrent des agents capables d'exécuter des pipelines mais trop conciliants sur l'argent, manipulables et aveugles au droit ; le régime réaliste est une file d'approbation hebdomadaire de 2 à 4 heures, pas zéro. La vente, et non la production, est le goulot : la médiane des expéditeurs d'e-mails à froid obtient une réponse pour 135 contacts, et les produits IA à moins de 50 USD par mois ne retiennent que 23 % de leur revenu. Trois verrous doivent être levés avant toute décision : l'autorisation écrite de l'employeur pour toute activité adjacente à la pharmacie, la confirmation écrite d'un marchand officiel acceptant un vendeur marocain, et le choix auto-entrepreneur contre SARL AU, qui détermine la capacité légale à payer les API étrangères.

## Conventions de lecture et niveaux de preuve

Chaque affirmation porte un niveau de preuve repris des notes des chercheurs. **[F]** désigne un fait lu sur la page primaire ou officielle le 11 novembre 2026. **[S]** désigne une source secondaire, un agrégateur, un blog de fournisseur ou un résumé de moteur de recherche : indicatif, à revérifier avant usage. **[AD]** désigne un revenu auto-déclaré par un fondateur ou affiché sur TrustMRR, non audité. **[H]** désigne une hypothèse économique du rédacteur ou des chercheurs. **[E]** désigne une estimation calculée à partir de faits et d'hypothèses explicites. **[I]** désigne une incertitude ou une information non vérifiable à ce stade. Les parts d'automatisation, les capitaux de départ et les niveaux de difficulté sont partout des estimations de chercheurs, jamais des mesures. Hypothèse de conversion utilisée dans tout le rapport, **à traiter comme une hypothèse et non comme un cours** : 1 USD ≈ 10 MAD (ordre de grandeur utilisé dans les notes), 1 EUR ≈ 11 MAD.

---

## A. Executive investment brief — la veille spécialisée gagne, l'autonomie totale n'existe pas

### Ce que la recherche établit

Le marché paie pour presque toutes les catégories de services IA, mais la preuve de revenu appartient à des éditeurs dotés d'équipes, pas à des opérateurs solo absents. Les chiffres les plus solides sont défavorables aux modèles faciles : les produits « IA-natifs » vendus moins de 50 USD par mois affichent une rétention brute médiane de **23 %**, contre **45 %** entre 50 et 249 USD et **70 %** au-dessus de 250 USD, où ils rejoignent le SaaS B2B classique [F] ([ChartMogul, déc. 2025](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)). Sur 8 699 startups suivies par TrustMRR, 3 787 déclarent un revenu et leur MRR médian est de **145 USD** [S] ([BigIdeasDB](https://bigideasdb.com/state-of-indie-saas-revenue-2026)) ; cet échantillon est lui-même biaisé vers le haut, puisque les fondateurs choisissent d'y figurer.

Les canaux d'acquisition automatisables se sont dégradés. L'expéditeur médian d'e-mails à froid obtient **0,74 % de réponses**, soit une réponse pour 135 contacts, sur 850 millions d'e-mails au premier semestre 2026 [F, source fournisseur] ([Smartlead](https://www.smartlead.ai/benchmarks)). Le taux de clic organique chute quand Google affiche un résumé IA (de 3,19 % à 1,31 % entre janvier et décembre 2025, remonté à 2,36 % en février 2026) [F] ([Seer Interactive](https://seerinteractive.com/insights/aio-impact-on-google-ctr-2026-update)), et la politique anti-spam de Google vise explicitement la production de masse de pages par IA générative [F] ([Google Search Central](https://developers.google.com/search/docs/essentials/spam-policies)). Les modèles « contenu IA en volume » sont donc éliminés presque en bloc.

Le Maroc ajoute un filtre que la plupart des guides ignorent. Stripe n'ouvre pas de compte marchand au Maroc (absent de sa liste de 51 marchés) [F] ([Stripe](https://stripe.com/global)), Google Play n'y autorise pas l'inscription marchand [F] ([Google Play Console](https://support.google.com/googleplay/android-developer/answer/9306917)), Shopify Payments n'y est pas disponible [F] ([Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/supported-countries)) et Polar ne verse pas au Maroc [F] ([Polar](https://polar.sh/docs/merchant-of-record/supported-countries)). À l'inverse, Lemon Squeezy liste le Maroc pour les virements bancaires [F] ([Lemon Squeezy](https://docs.lemonsqueezy.com/help/getting-started/supported-countries)) et Paddle ne l'exclut pas [F] ([Paddle](https://www.paddle.com/help/start/account-verification/which-countries-are-supported-by-paddle)). La réglementation des changes impose le rapatriement intégral des recettes d'export de services sous 90 jours et plafonne à **20 000 MAD par an** la dotation e-commerce d'un particulier pour payer par carte des fournisseurs étrangers [F] ([IGOC 2026, Office des Changes](http://www.oc.gov.ma/sites/default/files/2026-01/IGOC%202026_1.pdf)).

Enfin, l'autonomie complète n'est étayée par aucun cas. Dans Project Vend phase 2, les semaines à marge négative ont été « largement éliminées » seulement après l'ajout d'un CRM, de procédures de vérification et de liens de paiement ; l'agent « PDG » approuvait les demandes clémentes huit fois plus souvent qu'il ne les refusait, les remboursements ont triplé, et l'agent était prêt à signer un contrat contraire à une loi américaine [F] ([Anthropic, Project Vend 2](https://www.anthropic.com/research/project-vend-2)). Aucune de ces expériences n'a testé la partie difficile du cas présent : trouver des clients.

### Opportunités dominantes

| Rang révisé | Opportunité | Score révisé /100 | Pourquoi elle domine | Limite principale |
|---|---|---|---|---|
| 1 | Radar d'appels d'offres santé financés par les bailleurs (Afrique) | 60 | Données publiques, coût d'un oubli élevé pour l'acheteur, ancres de prix 49–342 USD/mois, pipeline déterministe | Conditions de réutilisation des portails non vérifiées ; acquisition sans appels non prouvée |
| 2 | Veille réglementaire cosmétiques / compléments alimentaires (Maroc, UE, Golfe) | 58 | Meilleur profil de conflit d'intérêts, turbulence réglementaire marocaine 2026, aucun concurrent tarifé identifié | Demande non prouvée ; disposition à payer purement hypothétique |
| 3 | Scrapers « Actors » sur Apify Store | 56 | Distribution et facturation intégrées, capital quasi nul, sous-produit des pipelines 1 et 2 | Revenus concentrés sur peu d'acteurs ; versement vers le Maroc non confirmé |
| 4 | Alertes TED santé / medtech (UE) | 54 | Seule source dont la réutilisation commerciale est vérifiée ; socle juridique propre pour démarrer | Marché banalisé dès 25 EUR/mois ; rétention faible sous 50 USD |
| 5 | Digest des tendances d'inspection GMP | 52 | Données openFDA en CC0, automatisation élevée | Facilement reproduit par un assistant généraliste ; ticket bas |

Les scores sont des jugements du rédacteur fondés sur les notes (section D), pas des mesures.

### Principales incertitudes

Cinq inconnues pèsent plus lourd que tout le reste. Premièrement, **aucun revenu vérifié n'existe** pour un opérateur solo dans la veille d'appels d'offres ou la veille réglementaire pharmaceutique : la preuve de demande se limite à l'existence de concurrents à prix publics. Deuxièmement, les conditions d'utilisation de marchespublics.gov.ma, de l'UNGM, de la Banque mondiale, de la BAD, du Fonds mondial et de l'UNICEF n'ont pas été lues. Troisièmement, la compatibilité du statut d'auto-entrepreneur avec un emploi salarié repose sur des guides commerciaux contradictoires, la loi 114-13 ne contenant aucune exclusion des salariés [F] ([Loi 114-13](https://adala.justice.gov.ma/api/uploads/2024/05/07/Loi%20Relative%20au%20statut%20de%20l%E2%80%99auto-entrepreneur-1715071318209.pdf)). Quatrièmement, le contrat de travail du mandant (clause d'exclusivité, politique d'activités extérieures) n'a pas été examiné. Cinquièmement, la conversion d'une réponse positive par e-mail en achat en libre-service sans appel n'est mesurée dans aucune source.

### Recommandations

Le mandant concentre capital et agents sur **un seul pipeline de veille mutualisé**, lancé d'abord sur la source juridiquement la plus propre (TED), étendu ensuite aux portails des bailleurs une fois leurs conditions vérifiées, puis dupliqué sur la veille cosmétiques/compléments. Il fixe les prix entre 79 et 149 USD par mois avec incitation au paiement annuel, parce que la rétention suit le prix et non l'ingéniosité du produit. Il exclut de la couverture tout produit, fournisseur, appel d'offres et client de son employeur, et obtient une autorisation écrite avant de vendre quoi que ce soit d'adjacent à la pharmacie. Il n'engage aucune dépense significative avant d'avoir obtenu des pilotes **payés** : les listes d'attente surestiment la demande de deux à trois ordres de grandeur (4 500 inscrits pour 5 clients payants dans un cas documenté) [S] ([mean.ceo](https://blog.mean.ceo/?p=11219)). Il réserve Fable 5.2 à une revue stratégique hebdomadaire, les données d'Anthropic montrant qu'il coûte 19 % de plus qu'Opus 5.5 comme orchestrateur pour un score équivalent [F] ([Anthropic, optimisation des coûts](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)).

---

## B. Market opportunity map — vingt-cinq familles, trois verdicts

Sept flux de recherche ont couvert vingt-cinq familles de modèles. Le tableau donne le verdict pour **ce mandant précis** (salarié pharma au Maroc, pas d'opérations quotidiennes, pas d'appels de vente), pas un jugement général sur la famille.

| # | Famille | Verdict | Preuve clé |
|---|---|---|---|
| 1 | Automatisations B2B par abonnement | Conditionnel | Défendable seulement comme pipeline déterministe au-dessus de 100 USD/mois ; sous 50 USD la rétention brute tombe à 23 % [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)) |
| 2 | Agences opérées par IA | À éviter | 11x : des employés décrivent 70–80 % de clients perdus [F] ([TechCrunch](https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have)) ; revenus par projet, le propriétaire devient l'opérateur [H chercheurs] |
| 3 | Micro-SaaS / SaaS vertical | Conditionnel | MRR médian 145 USD parmi les startups déclarant un revenu [S] ([BigIdeasDB](https://bigideasdb.com/state-of-indie-saas-revenue-2026)) ; 2 713 apps Shopify lancées en mai 2026 [S] ([BigIdeasDB](https://bigideasdb.com/shopify-app-vs-wordpress-plugin)) |
| 4 | Agents métiers (ticket élevé) | Conditionnel, hors mandat sans associé commercial | Rétention 70 % au-dessus de 250 USD/mois [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)), mais intégration et vente par conversations [H chercheurs] |
| 5 | Intelligence commerciale / réglementaire | **Attractif** | Trou de prix documenté : DrugPatentWatch 8 000–24 000 USD/an [F] ([DrugPatentWatch](https://www.drugpatentwatch.com/pricing/)) face à des petits outils à 69–149 USD/mois |
| 6 | Veille d'appels d'offres | **Attractif en niche**, banalisé en générique UE | Open Opportunities 160–342 USD/mois [F] ([OpenOpps](https://www.openopps.com/pricing)) ; Marchés Online dès 25 EUR/mois [F] ([Marchés Online](https://www.marchesonline.com/abonnement-entreprise)) |
| 7 | Produits numériques | Conditionnel (loterie) | Etsy Payments disponible au Maroc [F] ([Etsy](https://help.etsy.com/hc/articles/115015710408)) ; revenu médian Gumroad rapporté ~72 USD/mois [S, non vérifié] ([VoxBooster](https://voxbooster.com/blog/digital-course-sales-statistics-2026/)) |
| 8 | API et traitement de données | Conditionnel | Apify : 25 787 actors, 3 015 éditeurs actifs [S] ([SignalCensus](https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau)) ; RapidAPI prélève 25 % [S] ([RapidAPI](https://docs.rapidapi.com/docs/payouts-and-finance)) |
| 9 | Analyse documentaire | À éviter | Banalisée à 39–159 USD/mois [F] ([Docparser](https://www.docparser.com/pricing/)) ; ingère des documents clients, donc RGPD et questionnaires de sécurité [H chercheurs] |
| 10 | Génération de rapports | Conditionnel faible | Aucun opérateur nommé avec prix ou revenu publics ; les rapports ponctuels sont déjà absorbés par les assistants [H chercheurs] |
| 11 | Contenu, newsletters, médias de niche | Conditionnel (newsletter B2B payante) ; à éviter (sites à publicité) | Conversion médiane gratuit→payant 0,62 % à 10 USD/mois [F] ([beehiiv](https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026)) |
| 12 | Comparateurs / affiliation | À éviter | Politique « thin affiliation » [F] ([Google](https://developers.google.com/search/docs/essentials/spam-policies)) ; évaluer des produits non testés avec une IA est trompeur |
| 13 | SEO (comme activité) | À éviter | Outrank vend 30 articles pour 99 USD [F] ([Outrank](https://www.outrank.so/pricing)) ; SEObot −19,7 % de MRR en 30 jours [AD] ([first-mrr](https://first-mrr.com/study/seobot)) |
| 14 | Éducation | Conditionnel faible | Part instructeur du pool d'abonnement Udemy ramenée de 25 % à 15 % entre 2024 et 2026 [F] ([Udemy](https://teach.udemy.com/enabling-investment-subscription-terms-update/)) |
| 15 | E-commerce sans stock | À éviter | Shopify Payments indisponible au Maroc [F] ([Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/supported-countries)) ; ROAS de référence 1,86x [S, fournisseur] ([Triple Whale](https://triplewhale.com/blog/facebook-ads-benchmarks)) |
| 16 | Outils pour professions réglementées | À éviter | La politique d'usage d'Anthropic exige une revue humaine qualifiée pour les décisions individuelles en droit, médecine, finance [F, lu via résumé] ([Anthropic AUP](https://www.anthropic.com/legal/aup)) |
| 17 | Traduction / localisation | Conditionnel faible | Weglot dès 15 EUR/mois [F] ([Weglot](https://www.weglot.com/pricing)) |
| 18 | Veille de prix | Conditionnel | Prisync 99–399 USD/mois [F] ([Prisync](https://prisync.com/pricing/)) ; maintenance de scrapers et conditions des sites cibles |
| 19 | Prospection B2B « conforme » | À éviter | Prospection par e-mail soumise au consentement préalable au Maroc, sans exception B2B [F] ([CNDP](https://www.cndp.ma/wp-content/uploads/2025/07/fiche_CNDP_Prospection_RT_fr.pdf)) ; interdiction du spam par Anthropic [F] ([AUP](https://www.anthropic.com/legal/aup)) |
| 20 | Enrichissement de données | À éviter | Clay 167–446 USD/mois [F] ([Clay](https://www.clay.com/pricing)) ; sourcing licite des données personnelles non résolu |
| 21 | Automatisation du support | À éviter | Intercom Fin facture 0,99 USD par résolution [F] ([Intercom](https://www.intercom.com/pricing)) ; Chatbase 40–500 USD/mois [F] ([Chatbase](https://www.chatbase.co/pricing)) |
| 22 | Reporting non réglementé | Conditionnel faible | Preuve limitée à des éditeurs avec équipes (Cometly 196 525 USD MRR [AD]) ([TrustMRR](https://trustmrr.com/)) |
| 23 | Places de marché | Conditionnel comme canal (Apify, Shopify, Atlassian) ; loterie comme produit (job boards) | Job boards vérifiés Stripe de 11 USD à 9 400 USD de MRR [AD] ([TrustMRR](https://trustmrr.com/startup/findajobboard)) |
| 24 | Solutions PME Afrique / Europe | Conditionnel | 40 % des TPE/PME françaises utilisent une IA en 2026 [S] ([Blog du Modérateur](https://www.blogdumoderateur.com/ia-cyber-budgets-10-chiffres-numerique-tpe-pme-2026/)) ; au Maroc, 63 % des transactions restent en espèces [S] ([La Vie Éco](https://www.lavieeco.com/argent/le-paiement-digital-un-catalyseur-de-croissance-pour-les-tpme/)) |
| 25 | Outils pharma / médical / industriel | **Attractif** pour les produits d'information à faible conflit d'intérêts ; à éviter pour les outils GxP et les segments de l'employeur | AMMPS a repris les autorisations le 16 juin 2025 [S presse] ([Médias24](https://medias24.com/2025/06/10/autorisations-pharmaceutiques-lammps-reprend-les-attributions-du-sgg-des-le-16-juin/)) ; réforme PV/AMM 2026 [S presse] ([Médias24](https://medias24.com/2026/07/28/pharmacovigilance-amm-surveillance-du-marche-ce-qui-va-changer-1731843/)) |

Trois régularités traversent la carte. La forme des revenus se répète partout : un cas spectaculaire visible et une longue traîne mesurée près de zéro, que ce soit pour les extensions Chrome (38 extensions pour environ 31 USD de MRR dans un cas auto-déclaré) [AD] ([DEV Community](https://dev.to/_350df62777eb55e1/real-numbers-freemium-chrome-extension-monetization-after-6-months-5hga)) ou pour les newsletters. Les modèles vendables sans appel sont aussi ceux dont les prix sont les plus bas ; tout ce qui dépasse environ 1 000 USD par mois se vend visiblement par « réservez un appel », ce qui exclut le segment entreprise pour ce mandant. Enfin, « opérable par des agents » et « conforme aux règles d'authenticité des plateformes » tirent en sens opposé sur YouTube, Etsy, Medium, KDP et Google : plus la production est automatisée, plus elle se rapproche de la catégorie interdite.


---

## C. Exhaustive long list — 80 modèles distincts, 5 retenus, 32 conditionnels, 43 éliminés

Les sept notes inventorient 90 fiches (24 services B2B, 25 produits SaaS et données, 21 modèles de contenu et commerce, 20 niches pharma, réglementaires et appels d'offres). Après fusion des doublons (Apify, veille de prix, veille d'appels d'offres générique, données pharma, annuaires, modèles Notion, newsletters sponsorisées, comparateurs) et retrait d'une fiche qui décrit un schéma générique et non une opportunité (« service productisé par abonnement »), **le décompte réel est de 80 opportunités distinctes**. Aucune variante artificielle n'a été ajoutée pour atteindre un chiffre rond.

Lecture des colonnes. **Automatisation dominante** : A = automatique sans intervention humaine ordinaire ; B = automatique avec contrôle périodique ; C = validation humaine nécessaire pour les décisions sensibles ; D = difficilement automatisable, humain ou professionnel requis. Ces niveaux et le potentiel (faible / moyen / élevé) sont des estimations [H]. **Critères éliminatoires** : É1 illégal, trompeur ou contraire aux conditions d'une plateforme ; É2 dépend de la fraude, du spam ou de faux avis ; É3 aucune solution de paiement légale identifiée depuis le Maroc ; É4 dépend de données confidentielles non autorisées ou conflit d'intérêts frontal avec l'employeur ; É5 risque financier ou de responsabilité incontrôlable ; É6 pas de marché ou pas de canal d'acquisition crédible sans appels de vente ; É7 économie unitaire manifestement défavorable ; HM hors mandat (exige un opérateur quotidien ou vend des heures humaines).

### Services B2B productisés

| # | Opportunité | Marché / géographie | Modèle | Ancre de prix (sourcée) | Auto. | Potentiel | Blocage principal | Statut |
|---|---|---|---|---|---|---|---|---|
| 1 | Réceptionniste vocal IA pour PME francophones | France / UE | Abonnement mensuel | Rosie 49–299 USD/mois [F] ([Rosie](https://www.heyrosie.com/pricing)) ; Eliocall dès 79 EUR HT [S] ([La Fabrique du Net](https://www.lafabriquedunet.fr/logiciels/tech/standard-telephonique/standard-telephonique-ia)) | B | Moyen | Plancher de prix 30–50 USD, démonstration attendue, entrants financés | Conditionnelle |
| 2 | Revente d'agent vocal en marque blanche | PME | Abonnement | Synthflow : contrat annuel entreprise uniquement, plus de tarif à la minute [F] ([Synthflow](https://synthflow.ai/pricing)) | B | Faible | Le fournisseur change ses conditions ; marge fine | Éliminée É7 |
| 3 | AI SDR / prospection sortante gérée | B2B UE / US | 1 500–5 000 USD/mois | AiSDR 1,50 USD par prospect, service géré 2 500 USD/mois [F] ([AiSDR](https://aisdr.com/pricing/)) | C | Élevé en théorie | Attrition (cas 11x), proximité du spam, appels | Éliminée É2 + É5 |
| 4 | Listes de prospects à signaux d'intention | B2B UE / US | Abonnement | GojiberryAI 424 368 USD MRR [AD] ([TrustMRR](https://trustmrr.com/)) | B | Moyen | Conditions des sources de données, copie rapide | Conditionnelle (faible) |
| 5 | API de validation / enrichissement de contacts | Développeurs, monde | Usage | Clay 167–446 USD/mois [F] ([Clay](https://www.clay.com/pricing)) | A | Moyen | Sourcing licite, prix de commodité, acteurs installés | Éliminée É6 |
| 6 | Scrapers « Actors » sur Apify Store | Développeurs, agences, monde | Paiement à l'événement, 80 % au créateur | Créateur conserve 80 % moins le calcul [S, doc officielle] ([Apify](https://docs.apify.com/actors/monetize.md)) | B | Faible à moyen | Revenus concentrés, versement Maroc non confirmé | **Retenue** |
| 7 | Chatbot de support pour une niche | PME, e-commerce | Abonnement | Chatbase 40–500 USD/mois ; Fin 0,99 USD par résolution [F] ([Chatbase](https://www.chatbase.co/pricing), [Intercom](https://www.intercom.com/pricing)) | B | Faible | Le client se sert lui-même du même outil | Éliminée É7 |
| 8 | « Closer » DM en marque blanche | Agences | Abonnement | DM Champ 54 998 USD MRR [AD] ([TrustMRR](https://trustmrr.com/)) | C | Faible | Dépendance aux politiques Meta / WhatsApp | Éliminée É6 |
| 9 | Extraction documentaire mono-type | Back-offices | Abonnement | Docparser 39–159 USD/mois [F] ([Docparser](https://www.docparser.com/pricing/)) | B | Faible | Commodité ; documents clients confidentiels | Éliminée É7 |
| 10 | Préparation à la facturation électronique française | TPE / PME France | Service | Réception obligatoire offerte gratuitement par Tiime [S] ([Tiime](https://blog.tiime.fr/comparatif-plateformes-agreees-de-facturation-%C3%A9lectronique-en-2026)) | C | Faible | Ancre de prix à zéro ; l'expert-comptable possède le client | Éliminée É7 |
| 11 | Pré-comptabilité IA | Petites entreprises, cabinets | Abonnement | Dext ~31,50 USD/utilisateur/mois [S] ([Capterra](https://www.capterra.com/p/160189/Dext/pricing/)) | C | Faible | Frontière de la profession réglementée, responsabilité | Éliminée É7 |
| 12 | Service de réponse aux RFP | Vendeurs B2B | Abonnement | AutoRFP 899–1 299 USD/mois [S, blog fournisseur] ([AutoRFP](https://autorfp.ai/blog/loopio-pricing)) | C | Élevé | Vente par appels, base de connaissances client | Éliminée É6 |
| 13 | Veille d'appels d'offres + brouillon de mémoire technique (France) | PME françaises | Abonnement | Jorpex dès 49 USD/mois [S] ([Jorpex](https://jorpex.com/fr/compare/explore-alternative/)) | B | Moyen | Palmio, Explain, Olra ; veille gratuite CAPEB [S] ([CAPEB](https://www.capeb.fr/actualites/service-veille-marches-publics)) | Conditionnelle |
| 14 | Questionnaires de sécurité | Éditeurs SaaS | Annuel | Conveyor 9 600 USD/an [S, concurrent] ([Wolfia](https://connect.wolfia.com/blog/conveyor-reviews-pricing-alternatives)) | C | Élevé | Barrière de confiance pour un vendeur solo | Éliminée É6 |
| 15 | Veille de prix concurrentielle verticale | E-commerçants | Abonnement | Prisync 99–399 USD/mois selon volume [F] ([Prisync](https://prisync.com/pricing/)) | B | Moyen | Entretien des scrapers, conditions des sites | Conditionnelle |
| 16 | Réponse automatisée aux avis | Commerces multi-sites | Par établissement | RightResponse AI 10–44 USD/site/mois [S] ([Capterra UK](https://www.capterra.co.uk/software/1063362/rightresponse-ai)) | B | Faible | Plancher de prix ; ne jamais générer d'avis | Éliminée É7 |
| 17 | Localisation de sites FR-AR-EN | PME, SaaS | Abonnement / projet | Weglot dès 15 EUR/mois [F] ([Weglot](https://www.weglot.com/pricing)) | B | Faible | Prix plancher, litiges de qualité | Conditionnelle (faible) |
| 18 | Abonnement d'articles SEO générés | PME, SaaS | Abonnement | Outrank 99 USD pour 30 articles [F] ([Outrank](https://www.outrank.so/pricing)) | A | Faible | Saturation, mises à jour Google | Éliminée É7 |
| 19 | Audits et suivi GEO / AEO | Équipes marketing | Abonnement | Peec AI 95–495 USD/mois [F] ([Peec](https://peec.ai/pricing)) | B | Moyen | Outils nombreux, mesure instable ; la version service exige des appels | Conditionnelle (faible) |
| 20 | Agent publicitaire / reporting d'attribution | Annonceurs PME | Abonnement | Cometly 196 525 USD MRR [AD] ([TrustMRR](https://trustmrr.com/)) | C | Moyen | Responsabilité sur les dépenses publicitaires | Éliminée É5 |
| 21 | Infrastructure d'e-mails à froid | Équipes outbound | Abonnement | Instantly 47–358 USD/mois [F] ([Instantly](https://instantly.ai/pricing)) | B | Non estimé | Association au spam | Éliminée É2 |
| 22 | Automatisation LinkedIn | — | — | PROSP 128 005 USD MRR [AD] ([TrustMRR](https://trustmrr.com/)) | — | — | Interdite par LinkedIn [F] ([LinkedIn](https://www.linkedin.com/help/linkedin/answer/a1341387)) | Éliminée É1 |
| 23 | Agence d'automatisation sur mesure / freelancing IA | PME | Projets | Demande Upwork « AI Integration » +178 % [F, communiqué] ([Upwork](https://www.upwork.com/press/releases/upworks-in-demand-skills-2026-demand-for-top-ai-skills-more-than-doubles-as-ai-is-embedded-into-everyday-work)) | D | Moyen | Le propriétaire devient l'opérateur | Éliminée HM |

### Produits SaaS, API et données

| # | Opportunité | Marché / géographie | Modèle | Ancre de prix (sourcée) | Auto. | Potentiel | Blocage principal | Statut |
|---|---|---|---|---|---|---|---|---|
| 24 | App utilitaire Shopify | Marchands, monde | Abonnement ; 0 % de commission sur le premier million | 0 % jusqu'à 1 M USD cumulé, 15 % au-delà [S, doc officielle] ([Shopify.dev](https://shopify.dev/docs/apps/launch/distribution/revenue-share)) | B | Moyen (loterie) | 2 713 lancements par mois ; support ; versement Maroc non confirmé | Conditionnelle |
| 25 | App Atlassian Forge | Équipes B2B | Par utilisateur | 0 % jusqu'à 1 M USD de revenu Forge (temporaire) [S, officiel] ([Atlassian](https://www.atlassian.com/blog/developer/updates-to-marketplace-revenue-share-2026)) | B | Moyen | Revue de sécurité ; aucun revenu solo documenté | Conditionnelle |
| 26 | Extension Chrome | Grand public / pros | Freemium ou achat unique | Inscription 5 USD [S] ([9to5Google](https://9to5google.com/2020/03/12/chrome-web-store-fee/)) | B | Faible | Longue traîne proche de zéro | Conditionnelle (faible) |
| 27 | Plugin WordPress via Freemius | Sites WordPress | Licences annuelles | Frais Freemius ~7 % [S] ([Latka](https://getlatka.com/companies/freemius.com/interviews/freemius-vova-feldman-2025)) ; 10 % des produits d'un échantillon de 40 dépassent 1 000 USD/mois [S] ([BigIdeasDB](https://bigideasdb.com/how-to-sell-a-wordpress-plugin)) | B | Faible à moyen | Échantillon minuscule | Conditionnelle |
| 28 | App iOS à abonnement | Grand public | Abonnement | Commission 15 % (Small Business Program) [S] ([Apple](https://www.apple.com/in/newsroom/2020/11/apple-announces-app-store-small-business-program/)) | B | Faible | Versement Maroc non confirmé ; les apps IA perdent leurs abonnés ~30 % plus vite [S] ([TechCrunch](https://techcrunch.com/2026/03/10/ai-powered-apps-struggle-with-long-term-retention-new-report-shows)) | Conditionnelle (faible) |
| 29 | App Android payante / achats intégrés | — | — | Maroc : inscription développeur ✔, inscription marchand ✘ [F] ([Google Play](https://support.google.com/googleplay/android-developer/answer/9306917)) | — | — | Pas d'encaissement possible | Éliminée É3 |
| 30 | Apps HubSpot / Slack / AWS Marketplace | B2B | — | Aucun barème vérifié | B | Non estimable | Non instruit | Conditionnelle (non instruite) |
| 31 | API payante sur RapidAPI | Développeurs | Usage | Commission 25 %, versement PayPal uniquement [S] ([RapidAPI](https://docs.rapidapi.com/docs/payouts-and-finance)) | A | Faible | Commission, marché étroit | Conditionnelle (faible) |
| 32 | Points d'accès MCP sur un jeu de données de niche | Agents, développeurs | Usage | Aucun revenu documenté ; des actors exposent déjà un accès MCP ([Apify](https://apify.com/datapilot/public-tender-procurement-alerts/api/mcp)) | A | Non estimable | Aucune preuve de revenu | Conditionnelle (faible) |
| 33 | Données d'offres d'emploi / signaux d'embauche régionaux | Équipes commerciales, RH | Abonnement / API | TheirStack 49–59 USD/mois [S, sources en conflit] ([OpenWeb Ninja](https://www.openwebninja.com/blog/best-job-data-apis-2026)) | B | Faible | Marché mondial dense | Conditionnelle (faible) |
| 34 | API de données d'entreprises / registres | Conformité, vente | Annuel | OpenCorporates 2 250–12 000 GBP/an [S, page officielle] ([OpenCorporates](https://opencorporates.com/pricing/)) | B | Moyen | Licences de réutilisation des registres | Conditionnelle (faible) |
| 35 | Veille de conformité pour une verticale étroite (hors pharma) | Équipes conformité | Abonnement | Aucun prix trouvé | B | Non estimable | Demande non prouvée | Conditionnelle (non instruite) |
| 36 | Annuaire payant spécialisé | Sponsors, annonceurs | Référencements payants | 100 000 USD cumulés en 4 ans pour un cas [AD] ([Indie Hackers](https://www.indiehackers.com/post/i-built-a-simple-directory-of-job-boards-4-years-ago-it-just-passed-100k-60da9ba8f2)) | B | Faible | Dépendance au SEO | Conditionnelle (faible) |
| 37 | Boilerplate / kit de démarrage | Développeurs | Vente unique | Dirstarter ~5 000 USD/mois [AD] ([Indie Hackers](https://www.indiehackers.com/post/how-i-turned-my-copycats-into-customers-from-open-source-directory-to-5k-month-boilerplate-ce615af4f6)) | B | Faible | Suit une audience existante | Éliminée É6 |
| 38 | Modèles Notion / Canva, packs de ressources (Gumroad) | Créateurs | Vente unique | Gumroad 10 % + 0,50 USD [S] ([GlobalSolo](https://www.globalsolo.global/blog/stripe-vs-paddle-vs-lemon-squeezy-2026)) | B | Faible | Pas de demande intégrée ; packs de prompts interdits sur Etsy | Éliminée É6 |
| 39 | Site comparatif / affiliation | — | Commissions | Amazon ~2,5–4,5 % sur les grandes catégories [S] ([Lasso](https://getlasso.co/amazon-affiliate-commission-rate/)) | A | Faible | « Thin affiliation » ; avis sans test = trompeur | Éliminée É1 + É7 |
| 40 | Newsletter gratuite financée par sponsors | Annonceurs | CPM | Newsletter de 92 000 abonnés vendue 20 500 USD avec ~300 USD de revenu sponsor [F] ([Microns](https://newsletter.microns.io/p/2025-year-in-review)) | B | Faible | Exige des dizaines de milliers d'abonnés engagés | Éliminée É7 |
| 41 | Agent vertical à ticket élevé (> 250 USD/mois) | B2B | Abonnement | Rétention brute 70 % dans cette bande [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)) | C | Élevé | Intégration et vente par conversations | Éliminée HM + É6 |
| 42 | Wrapper IA à bas prix (< 50 USD/mois) | Grand public | Abonnement | Rétention brute 23 % [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)) | A | Faible | Les clients le traitent comme un essai | Éliminée É7 |
| 43 | Micro-SaaS vertical à ticket moyen (50–249 USD/mois) | B2B | Abonnement | Rétention brute 45 %, nette 61 % [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)) | B | Moyen | Acquisition | Conditionnelle (bande de prix des modèles retenus) |
| 44 | Rachat et amélioration d'un micro-actif | — | Acquisition | App Shopify à 1 900 USD de revenu annuel proposée 5 500 USD [F] ([Microns](https://newsletter.microns.io/p/2025-year-in-review)) ; médiane demandée ~190 000 USD sur Acquire.com [S] ([BigIdeasDB](https://bigideasdb.com/state-of-saas-valuations-2026)) | C | Faible | Sélection adverse sous 10 000 USD ; paiement en devises non étudié | Conditionnelle (faible) |

### Contenu, audience et commerce

| # | Opportunité | Marché / géographie | Modèle | Ancre de prix (sourcée) | Auto. | Potentiel | Blocage principal | Statut |
|---|---|---|---|---|---|---|---|---|
| 45 | Newsletter B2B / finance payante | Professionnels, monde | Abonnement | Médiane 10 USD/mois ; investissement 27 USD/mois ; conversion médiane 0,62 % [F] ([beehiiv](https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026)) | B | Faible à moyen | Constituer la liste ; encaissement souvent lié à Stripe [I] | Conditionnelle |
| 46 | Substack grand public | Lecteurs | Abonnement | Substack prélève 10 % [S] ([Press Gazette](https://pressgazette.co.uk/newsletters/newsletters-2026-prices-retention-churn/)) | D | Faible | Porté par une personnalité ; détection IA côté lecteur depuis juillet 2026 | Éliminée É6 |
| 47 | Site média à publicité, contenu IA | Régies | Publicité | Petits éditeurs : −60 % de trafic de recherche Google [S, correspondance non vérifiée] ([Let's Data Science](https://letsdatascience.com/news/googles-ai-search-features-cut-publisher-traffic-data-from-s-d1c19012)) | A | Faible | « Scaled content abuse » [F] ([Google](https://developers.google.com/search/docs/essentials/spam-policies)) | Éliminée É1 + É7 |
| 48 | SEO programmatique comme activité | — | Publicité / affiliation | Même politique Google [F] ([Google](https://developers.google.com/search/docs/essentials/spam-policies)) | A | Faible | Viable seulement si les pages exposent des données propres (alors c'est un canal, pas un produit) | Éliminée É7 |
| 49 | Chaîne YouTube « faceless » longue durée | Annonceurs | Partage publicitaire 55 % | RPM médian 2,30 USD sur 300 chaînes déjà établies [S, fournisseur] ([AIR](https://air.io/en/air-data-findings/youtube-monetization-statistics-2026)) | C | Faible | Contenu « inauthentique » non monétisable [F] ([YouTube](https://support.google.com/youtube/answer/1311392)) | Éliminée É7 |
| 50 | Automatisation de YouTube Shorts | Annonceurs | Partage publicitaire | RPM 0,02–1,48 USD [S] ([AIR](https://air.io/en/air-data-findings/youtube-monetization-statistics-2026)) | A | Faible | Économiquement négligeable | Éliminée É7 |
| 51 | Réseau de podcasts générés par IA | Annonceurs | Publicité | ~35,4 % des nouveaux flux probablement générés par IA [S] ([Podnews](https://podnews.net/update/ai-slop-overtakes-humans)) | A | Faible | Un acteur industriel inonde déjà la longue traîne | Éliminée É6 |
| 52 | Images / vidéos / musiques de stock générées | Banques d'images | Redevances | Recul de la ligne Stock d'Adobe attribué à l'IA générative [S] ([Barchart](https://www.barchart.com/story/news/730560/adbe-q1-deep-dive-ai-transition-ceo-succession-and-freemium-push-shape-outlook)) | A | Faible | La demande elle-même est substituée | Éliminée É6 |
| 53 | Livres Amazon KDP écrits par IA | Lecteurs | Redevances | Divulgation IA obligatoire [F] ([KDP](https://kdp.amazon.com/en_US/help/topic/G200672390)) ; plafond de 3 titres/jour [S] ([Authors Guild](https://authorsguild.org/news/amazon-adds-to-kdp-generative-ai-policy-caps-daily-self-publishing-uploads/)) | B | Faible | Inondation ; aucune distribution de revenus trouvée | Éliminée É6 |
| 54 | Téléchargements numériques Etsy (créations originales) | Consommateurs | Vente unique | Frais 6,5 % + 0,20 USD ; traitement Maroc 4,5 % + 5 MAD [S] ([WorldFirst](https://www.worldfirst.com/af/blog/online-sellers/how-does-etsy-pay-you-africa/)) | B | Faible | Saturation ; règles durcies trimestre après trimestre [F] ([Etsy](https://www.etsy.com/legal/creativity)) | Conditionnelle (loterie) |
| 55 | Cours Udemy dans une niche d'expertise | Apprenants | Part de 37 % | Pool d'abonnement instructeur réduit à 15 % en janvier 2026 [F] ([Udemy](https://teach.udemy.com/enabling-investment-subscription-terms-update/)) | C | Faible | L'intrant rare est l'expertise humaine ; conflit d'intérêts si sujet pharma | Conditionnelle (faible) |
| 56 | Cours auto-hébergé / cohorte | Apprenants | Vente | Prix médian 110 USD [S, fournisseur] ([Ruzuku](https://www.ruzuku.com/learn/articles/course-pricing-benchmarks)) | D | Faible | Exige une audience ; les cohortes ne s'automatisent pas | Éliminée É6 |
| 57 | Impression à la demande sur Etsy | Consommateurs | Marge | Marges « visées » 20–40 % (chiffre d'un fournisseur POD) [S] ([Printful](https://www.printful.com/blog/print-on-demand-statistics)) | B | Faible | Marges fines après frais et publicité | Conditionnelle (faible) |
| 58 | Dropshipping / POD sur boutique Shopify avec publicité | Consommateurs | Marge | CPM Meta médian 14,19 USD, ROAS 1,86x [S, fournisseur] ([Triple Whale](https://triplewhale.com/blog/facebook-ads-benchmarks)) | C | — | Shopify Payments indisponible ; capital publicitaire | Éliminée É3 + É5 + É7 |
| 59 | Job board de niche | Employeurs | Annonces payantes | De 11 USD à 9 400 USD de MRR [AD] ([TrustMRR](https://trustmrr.com/startup/qatestingjobs-com), [TrustMRR](https://trustmrr.com/startup/findajobboard)) | B | Faible à moyen | Démarrage biface ; dépendance SEO | Conditionnelle |
| 60 | Medium Partner Program avec texte IA | — | — | Texte généré par IA interdit derrière le paywall depuis le 1er mai 2024 [F] ([Medium](https://help.medium.com/hc/en-us/articles/22576852947223)) | — | — | Fermé par la politique | Éliminée É1 |

### Pharma, médical, réglementaire, appels d'offres

Le risque de conflit d'intérêts (COI) est repris des notes pour un salarié de l'industrie pharmaceutique marocaine ; il se réévalue au vu du périmètre réel de l'employeur, inconnu à ce stade [I].

| # | Opportunité | Marché / géographie | Modèle | Ancre de prix (sourcée) | Auto. | Potentiel | Blocage principal | Statut |
|---|---|---|---|---|---|---|---|---|
| 61 | Veille réglementaire pharma Maroc / Maghreb | ~50–60 laboratoires, importateurs, cabinets | 100–400 USD/mois [H] | Cortellis estimé à 20 000 USD/an et plus [S, blog non vérifié] ([arblogz](https://arblogz.pages.dev/blog/clarivate-lsh-division-sale-cortellis-cri)) | B | Moyen | **COI élevé** : même régulateur, mêmes pairs que l'employeur | Conditionnelle (autorisation écrite préalable) |
| 62 | Intelligence réglementaire panafricaine francophone | Exportateurs de génériques, ONG | 150–500 USD/mois [H] | AgencyIQ lancé à 25 000–75 000 USD/an en 2020 [F, ancien] ([Digiday](https://digiday.com/media/politicos-new-fda-focused-subscription-product-costs-75k-year/)) | C | Moyen à élevé | Sources en PDF non lisibles par machine ; COI moyen à élevé | Conditionnelle |
| 63 | Radar d'appels d'offres pharma Maroc avec historique d'attribution | Laboratoires, distributeurs | 6 000–25 000 MAD/an [S] | Veille marocaine générique 6 000–25 000 MAD/an [S, blog fournisseur] ([Kolonell](https://kolonell.com/fr/blog/plateforme-gestion-appels-offres-btp-casablanca-cout-2026)) | B | Moyen | **COI très élevé** si l'employeur soumissionne : le piège le plus net de la liste | Éliminée É4 |
| 64 | Radar d'appels d'offres santé des bailleurs en Afrique (UNGM, Banque mondiale, BAD, Fonds mondial, UNICEF) | Exportateurs, distributeurs, fournisseurs d'ONG | 50–300 USD/mois [H] | Open Opportunities 160–342 USD/mois [F] ([OpenOpps](https://www.openopps.com/pricing)) | B | Moyen | Conditions des portails non vérifiées ; acquisition | **Retenue** |
| 65 | Alertes TED verticales santé / pharma / medtech | PME exportatrices, y compris Maghreb | 25–150 EUR/mois | Marchés Online dès 25 EUR/mois [F] ([Marchés Online](https://www.marchesonline.com/abonnement-entreprise)) ; Jorpex 49–149 USD/mois [S] ([Jorpex](https://jorpex.com/compare/tender-monitoring-tools/)) | B | Faible à moyen | Marché encombré ; seule la profondeur verticale différencie | **Retenue** (comme module) |
| 66 | Briefings « opportunités génériques » / expirations de brevets | Équipes BD de génériqueurs | 200–500 USD/mois ou 1 000–3 000 USD par rapport [H] | DrugPatentWatch 8 000–24 000 USD/an [F] ([DrugPatentWatch](https://www.drugpatentwatch.com/pricing/)) | C | Élevé | **COI très élevé** : savoir-faire BD de l'employeur ; frontière de l'avis juridique | Éliminée É4 |
| 67 | Intelligence de sourcing API / fournisseurs | Achats et AQ de petits génériqueurs | 100–300 USD/mois [H] | PharmaCompass gratuit, financé par les fournisseurs [F] ([PharmaCompass](https://www.pharmacompass.com/manufacturers-suppliers-distributors-services-fdf)) | B | Moyen | **COI très élevé** ; risque de diffamation en notant des fournisseurs | Éliminée É4 |
| 68 | Digest des tendances d'inspection GMP | Responsables AQ, marchés émergents | 50–200 USD/mois [H] | Newsletter FDAnews 1 895 USD/an [F, page non revérifiée] ([FDAnews](https://www.fdanews.com/subscriptions)) | B | Faible à moyen | Reproductible par un assistant ; COI moyen | **Retenue** (comme module) |
| 69 | Assistant de rédaction SOP / déviations / CAPA | Petits fabricants, distributeurs | 100–500 USD/mois [H] | RAi 1 500 USD/mois [F, provenance incertaine] ([RAi](https://rai-3d8.pages.dev/)) | C | Moyen | Qualification fournisseur par l'AQ ; ne peut être le système GxP de référence | Éliminée É6 |
| 70 | Service de mise en forme CTD et contrôle d'écarts | Petits titulaires d'AMM | Par dossier | Freyr SUBMIT PRO ~1 750 par utilisateur et par mois [S, agrégateur] ([GetApp](https://www.getapp.com/operations-management-software/a/freyrsubmitpro/)) | D | Moyen | Responsabilité de conseil ; COI élevé | Éliminée É4 + HM |
| 71 | Veille de littérature locale en pharmacovigilance | Petits titulaires, prestataires PV | 100–400 USD/mois [H] | Bibliovigilance dès 119 USD/mois [S] ([GetApp](https://www.getapp.com/all-software/a/bibliovigilance/)) | C | Moyen | Un cas manqué = constat de non-conformité ; processus validé exigé | Éliminée É5 |
| 72 | Desk de rédaction médicale | CRO, affaires médicales | Par livrable | Rédacteurs seniors 140–350 USD/h [S, guide promotionnel] ([Jobbers](https://www.jobbers.io/medical-writing-freelancing-pharma-healthcare-regulatory-content-2026/)) | D | Moyen | Vend du temps humain | Éliminée HM |
| 73 | Veille conformité cosmétiques et compléments alimentaires (Maroc / UE / Golfe) | Centaines de petites marques et importateurs | 50–200 USD/mois [H] | Aucun concurrent tarifé identifié | B | Moyen | Demande non prouvée | **Retenue** |
| 74 | Navigateur d'enregistrement des dispositifs médicaux (Maroc + Afrique francophone) | Importateurs, PME étrangères | Par dossier + abonnement | Consultants 150–450 USD/h [S] ([MedDeviceGuide](https://meddeviceguide.com/blog/medical-device-regulatory-consulting-hourly-rates-region-guide)) | C | Moyen | Pas de représentation légale ; canal SEO entrant érodé | Conditionnelle |
| 75 | Moniteur de pénuries et de changements de prix des médicaments | Grossistes, pharmacies, acheteurs hospitaliers | 10–50 USD/mois [H] | pharmazie.com 50–250 EUR/utilisateur/mois [S] ([pharmazie.com](https://go.pharmazie.com/pricing)) | B | Faible | Ticket bas ; COI élevé s'il expose les produits de l'employeur | Conditionnelle (faible) |
| 76 | Outils back-office IA pour pharmacies | 14 134 pharmacies au Maroc [S] ([Le Desk](https://ledesk.ma/datadesk/distribution-du-medicament-les-limites-chiffrees-du-modele-selon-le-conseil-de-la-concurrence/)) | Abonnement | Prix des éditeurs locaux non trouvés | D | Faible | Vente terrain, faible revenu par client, données de santé (CNDP) | Éliminée É6 + HM |
| 77 | Intelligence import / export et douanes des produits de santé | Exportateurs, négociants | 100–300 USD/mois ou rapports [H] | Volza 125–800 USD/mois [S, agrégateur] ([Toolradar](https://toolradar.com/tools/volza/pricing)) | B | Moyen | Licences de revente des données douanières | Conditionnelle |
| 78 | Fiches d'accès au marché Afrique / MENA | PME étrangères | 300–1 500 USD par rapport [H] | Acteurs installés uniquement sur devis ([Evaluate](https://www.evaluate.com/pricing/)) | C | Moyen | Les rapports ponctuels sont absorbés par les assistants | Conditionnelle |
| 79 | Veille d'appels d'offres générique pour PME marocaines (hors pharma) | 54 000 entreprises inscrites au portail [S presse] ([TelQuel](https://telquel.ma/instant-t/2026/05/21/marches-publics-nadia-fettah-annonce-54-000-entreprises-inscrites-et-une-hausse-de-408-des-bons-de-commande_1990710/)) | 6 000–25 000 MAD/an [S] | Idem #63 ([Kolonell](https://kolonell.com/fr/blog/plateforme-gestion-appels-offres-btp-casablanca-cout-2026)) | B | Moyen | Vente locale par téléphone / WhatsApp [H] ; conditions du portail non vérifiées ; prospection sur consentement | Conditionnelle |
| 80 | Intelligence de sourcing industriel B2B | Acheteurs de PME | Par mission | Aucune ancre trouvée | D | Faible | Service à la mission ; recouvre le savoir-faire achats | Éliminée HM |

### Modèles éliminés, regroupés par critère

Quarante-trois modèles sortent, pour sept raisons. **Illégal, trompeur ou contraire aux conditions d'une plateforme (É1)** : automatisation LinkedIn (#22), comparateurs d'affiliation fondés sur des avis non testés (#39), sites de contenu IA en volume (#47), Medium avec texte généré (#60). **Dépendance au spam (É2)** : AI SDR (#3) et infrastructure d'e-mails à froid (#21), que la politique d'usage d'Anthropic place au contact de l'interdiction du spam ([Anthropic AUP](https://www.anthropic.com/legal/aup)). **Aucun paiement légal depuis le Maroc (É3)** : apps Android payantes (#29), dropshipping sur Shopify (#58). S'y ajoutent deux montages que le rapport écarte comme contournements : la société américaine avec compte Stripe, que l'instruction des changes soumet à autorisation pour un résident marocain [F] ([IGOC 2026](http://www.oc.gov.ma/sites/default/files/2026-01/IGOC%202026_1.pdf)), et l'encaissement en crypto-actifs, sans loi en vigueur [S presse] ([Hespress](https://fr.hespress.com/470286-cryptomonnaie-le-gouvernement-accelere-la-regulation-pour-contrer-le-blanchiment-et-encadrer-le-marche.html)). **Données confidentielles ou conflit d'intérêts frontal (É4)** : radar d'appels d'offres pharma Maroc (#63), briefings de brevets (#66), sourcing de principes actifs (#67), mise en forme CTD (#70). **Risque incontrôlable (É5)** : agents publicitaires (#20), veille PV (#71), et à nouveau #3 et #58. **Pas de marché ou de canal sans appels (É6)** : #5, #8, #12, #14, #37, #38, #41, #46, #51, #52, #53, #56, #69, #76. **Économie unitaire défavorable (É7)** : #2, #7, #9, #10, #11, #16, #18, #40, #42, #48, #49, #50. **Hors mandat (HM)** : agence sur mesure (#23), rédaction médicale (#72), sourcing industriel (#80).


---

## D. Top 20 opportunities — le classement initial, puis ce que la contre-expertise en laisse

### Grille et classement initial

La grille pèse sept critères pour 100 points : potentiel de profit net (25), autonomie opérationnelle (20), vitesse de validation commerciale (15), efficacité du capital (10), défendabilité et croissance (10), faisabilité de l'acquisition client (10), compatibilité juridique, bancaire et opérationnelle avec le Maroc (10). **Les notes sont des jugements du rédacteur à partir des preuves des sept notes de recherche ; aucune n'est une mesure.** Le critère « Maroc » intègre le conflit d'intérêts avec l'employeur.

| Rang | Opportunité (# liste) | Profit /25 | Auton. /20 | Valid. /15 | Capital /10 | Défend. /10 | Acquis. /10 | Maroc /10 | Total | Justification en une ligne |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Radar AO santé bailleurs Afrique (#64) | 14 | 16 | 10 | 8 | 6 | 5 | 7 | **66** | Ancres 49–342 USD/mois, données publiques, oubli coûteux pour l'acheteur, COI moyen |
| 2 | Actors Apify (#6) | 8 | 17 | 12 | 10 | 3 | 8 | 6 | **64** | Distribution et facturation intégrées, capital < 200 USD, maintenance adaptée aux agents |
| 3 | Alertes TED santé / medtech (#65) | 9 | 18 | 10 | 9 | 3 | 5 | 8 | **62** | Réutilisation commerciale de TED vérifiée, flux XML et API gratuits, automatisation ~90 % |
| 4 | Veille cosmétiques / compléments (#73) | 12 | 15 | 9 | 8 | 6 | 5 | 6 | **61** | Meilleur profil COI, turbulence réglementaire 2026, pas de concurrent tarifé |
| 5 | Digest inspections GMP (#68) | 8 | 17 | 9 | 9 | 4 | 5 | 6 | **58** | openFDA en CC0, pipeline simple, contenu éducatif à faible responsabilité |
| 6 | Veille réglementaire pharma Maroc (#61) | 12 | 14 | 8 | 8 | 7 | 6 | 2 | **57** | Adéquation maximale à l'expertise, mais même régulateur et mêmes pairs que l'employeur |
| 7 | Veille AO + mémoire technique France (#13) | 10 | 14 | 9 | 8 | 3 | 5 | 8 | **57** | Prospection B2B par e-mail admise en France, marché prouvé mais dense |
| 8 | App Shopify (#24) | 10 | 13 | 8 | 9 | 5 | 6 | 5 | **56** | 0 % de commission, confiance transférée par la plateforme, résultat de loterie |
| 9 | App Atlassian Forge (#25) | 11 | 13 | 6 | 9 | 6 | 6 | 5 | **56** | Acheteurs B2B par utilisateur, moins d'entrants, revue de sécurité |
| 10 | Intelligence réglementaire panafricaine (#62) | 14 | 12 | 6 | 7 | 7 | 4 | 5 | **55** | Sources fragmentées = barrière, mais automatisation 60–70 % et COI moyen à élevé |
| 11 | Navigateur dispositifs médicaux (#74) | 10 | 12 | 7 | 8 | 5 | 4 | 7 | 53 | Procédures AMMPS mal documentées en anglais ; COI faible si employeur « médicament seul » |
| 12 | Veille AO générique PME Maroc (#79) | 10 | 15 | 8 | 8 | 4 | 3 | 5 | 53 | 54 000 entreprises inscrites, ancre 6 000–25 000 MAD/an, vente locale difficile sans appels |
| 13 | Veille de prix verticale (#15) | 9 | 16 | 7 | 8 | 3 | 3 | 7 | 53 | Prix publics 99–399 USD/mois, entretien de scrapers |
| 14 | Plugin WordPress Freemius (#27) | 6 | 14 | 7 | 9 | 4 | 6 | 7 | 53 | Freemius liste le Maroc ; 10 % des produits au-dessus de 1 000 USD/mois dans un petit échantillon |
| 15 | Téléchargements Etsy (#54) | 4 | 11 | 11 | 10 | 2 | 6 | 9 | 53 | Paiement natif vers le Maroc, premier revenu en 1–3 mois [H], saturation |
| 16 | Fiches d'accès au marché Afrique / MENA (#78) | 9 | 11 | 9 | 8 | 4 | 4 | 6 | 51 | 300–1 500 USD par rapport [H], mais ponctuel et substituable |
| 17 | Newsletter B2B payante (#45) | 7 | 13 | 8 | 9 | 5 | 3 | 5 | 50 | 16 000 abonnés gratuits nécessaires pour ~1 000 USD/mois à la médiane |
| 18 | Job board de niche (#59) | 7 | 15 | 6 | 9 | 4 | 3 | 6 | 50 | Quelques réussites vérifiées, longue traîne à 11–58 USD de MRR |
| 19 | Cours Udemy d'expertise (#55) | 5 | 8 | 8 | 10 | 4 | 7 | 6 | 48 | La plateforme apporte la demande ; l'intrant est le temps de l'expert |
| 20 | Intelligence import / export santé (#77) | 9 | 12 | 6 | 6 | 5 | 4 | 5 | 47 | Volza 125–800 USD/mois, mais licences de données restrictives |

### Seconde passe contradictoire sur le top 10

Chaque opportunité du top 10 répond aux huit mêmes questions. Les arguments viennent de la note « red team » : rétention des produits IA bon marché, médianes de l'e-mail à froid, résumés IA de Google, rails de paiement marocains, conflit d'intérêts avec l'employeur, absence d'entreprise entièrement autonome documentée.

**1. Radar d'appels d'offres santé des bailleurs en Afrique (#64) — 66 → 60**

| Question | Réponse |
|---|---|
| Pourquoi échouer malgré une bonne proposition de valeur ? | Le produit se construit en semaines, mais personne ne l'achète sans preuve de complétude ; aucun revenu d'opérateur solo n'est documenté dans cette niche |
| Le marché est-il saturé ? | Les généralistes existent (Open Opportunities, TendersOnTime, Tendersinfo, GlobalTenders, L2B) mais sans appariement par molécule, DCI ou préqualification OMS et avec un français faible [H chercheurs] |
| Concurrents mieux financés ? | Oui pour la couverture mondiale ; non identifiés sur la couche verticale santé francophone |
| Pourquoi pas ChatGPT ou Claude ? | Le client le testera avec une requête de dix minutes ; le produit ne passe que si sa couverture est démontrablement plus complète qu'une recherche approfondie planifiée, et s'il assume la responsabilité des oublis |
| Quelle part d'automatisation est réellement difficile ? | Le rappel (ne rien manquer) sur des portails hétérogènes, et l'appariement fin avec le catalogue de chaque client |
| Quel coût peut détruire la rentabilité ? | Pas les jetons (ordre de 25–45 USD/mois [E]) : le coût fixe d'une SARL AU (15 000–50 000 MAD/an [S]) et le coût d'acquisition si l'on bascule sur du payant (CAC PPC ~802 USD [S]) |
| Hypothèse commerciale la plus fragile ? | Qu'un exportateur réponde à un e-mail automatisé et paie en libre-service sans appel : aucune source ne mesure cette conversion |
| Comment vérifier la demande avant de dépenser ? | Digest « concierge » gratuit pendant deux à trois semaines pour 10 à 20 prospects nommés, puis lien de paiement ; critère fixé en argent |

Révision : profit 14 → 12 (univers d'acheteurs non dénombré), validation 10 → 8, acquisition 5 → 4 (médiane 0,74 % de réponses), Maroc 7 → 6 (conditions des portails non lues, COI à borner).

**2. Actors Apify (#6) — 64 → 56**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Un développeur rapporte 0 USD de revenu malgré 5 407 résultats livrés, ses utilisateurs étant sur l'offre gratuite [AD] ([DEV Community](https://dev.to/sessionzero_ai/2000-runs-in-3-days-real-revenue-data-from-launching-13-korean-scrapers-on-apify-211h)) |
| Saturé ? | 25 787 actors et 3 015 éditeurs actifs en mai 2026 [S] ([SignalCensus](https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau)) |
| Concurrents mieux financés ? | Non pertinent : la concurrence est une foule de solos ; des actors d'appels d'offres existent déjà à 10 USD/mois ou 0,10 USD les 1 000 résultats [S] ([Apify](https://apify.com/taroyamada/procurement-intel-actor/api/mcp)) |
| Pourquoi pas ChatGPT ou Claude ? | L'acheteur est un développeur : la vraie question est « pourquoi ne pas le scraper moi-même avec un agent » |
| Automatisation difficile ? | La réparation quand le site cible change, et le respect des conditions de chaque cible |
| Coût destructeur ? | Le calcul de plateforme déduit des 80 % ; les frais et le change PayPal |
| Hypothèse fragile ? | Que les versements atteignent un compte marocain (minimum 20 USD par PayPal, 100 USD autrement [S] ([Apify](https://docs.apify.com/actors/publishing/monetize/monthly-payouts.md))) : non confirmé |
| Vérifier la demande ? | Compter les concurrents, leur volume d'exécutions et leurs prix sur la place de marché avant d'écrire une ligne ; un à deux jours, gratuit |

Révision : profit 8 → 5, validation 12 → 10, défendabilité 3 → 2, acquisition 8 → 7, Maroc 6 → 5.

**3. Alertes TED santé / medtech (#65) — 62 → 54**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | L'alerte brute est une commodité ; les prix d'entrée sont déjà à 25 EUR/mois avec des offres gratuites |
| Saturé ? | Oui : Marchés Online, Stotles (offre gratuite), Tenders Direct, Jorpex, Tracker |
| Concurrents mieux financés ? | Oui (Infopro, Stotles, Mercell) |
| Pourquoi pas ChatGPT ou Claude ? | TED est ouvert, structuré et interrogeable par API : c'est précisément le cas qu'un assistant planifié couvre bien |
| Automatisation difficile ? | Peu de chose ; la difficulté est commerciale |
| Coût destructeur ? | Les frais du marchand officiel pèsent ~6 % à 45 USD ; l'attrition coûte davantage : sous 50 USD la rétention brute médiane est de 23 % [F] |
| Hypothèse fragile ? | Qu'une couche verticale santé justifie un prix supérieur aux généralistes |
| Vérifier la demande ? | L'utiliser d'abord comme démonstrateur et échantillon gratuit du radar #64, pas comme produit autonome |

Révision : profit 9 → 6, validation 10 → 8, défendabilité 3 → 2, acquisition 5 → 3. Le critère Maroc reste à 8 : c'est la source la plus propre juridiquement [F] ([TED](https://ted.europa.eu/en/help/data-reuse)).

**4. Veille conformité cosmétiques / compléments (#73) — 61 → 58**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | L'absence de concurrent tarifé signifie aussi l'absence de preuve que quelqu'un paie |
| Saturé ? | Non d'après les notes, mais la recherche n'a pas dénombré les marques ni les importateurs |
| Concurrents mieux financés ? | Aucun identifié ; la presse spécialisée et les cabinets de conseil sont les substituts |
| Pourquoi pas ChatGPT ou Claude ? | Les textes marocains (AMMPS, ONSSA, Bulletin officiel) sont fragmentés et en évolution ; un assistant les trouve mal, mais un client motivé peut s'en contenter |
| Automatisation difficile ? | L'interprétation « que dois-je faire et pour quand » sans glisser vers le conseil réglementaire |
| Coût destructeur ? | Aucun côté production ; le risque est un revenu nul sur des coûts fixes de ~120 USD/mois [E] |
| Hypothèse fragile ? | Que de petites marques marocaines paient 50–200 USD/mois par carte, dans un pays où 63 % des transactions sont en espèces [S] |
| Vérifier la demande ? | Trois numéros gratuits d'un bulletin sur la réforme des compléments de 2026, puis prévente annuelle |

Révision légère : profit 12 → 11, validation 9 → 8, acquisition 5 → 4. La prospection de contacts marocains par e-mail exige un consentement préalable [F] ([CNDP](https://www.cndp.ma/wp-content/uploads/2025/07/fiche_CNDP_Prospection_RT_fr.pdf)), ce qui oriente l'acquisition vers les associations professionnelles et le contenu.

**5. Digest des tendances d'inspection GMP (#68) — 58 → 52**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Un digest récurrent de pages publiques figure dans la liste des usages déjà banalisés par les assistants |
| Saturé ? | Redica, FDAnews, Govzilla au-dessus ; contenus gratuits en dessous |
| Concurrents mieux financés ? | Oui (Redica) |
| Pourquoi pas ChatGPT ou Claude ? | Objection forte : les données sont publiques, en anglais, structurées |
| Automatisation difficile ? | Aucune partie réellement difficile, ce qui signifie aussi aucune barrière |
| Coût destructeur ? | L'attrition : le ticket probable tombe dans la bande 23–45 % de rétention |
| Hypothèse fragile ? | Qu'un responsable AQ paie de sa carte pour une synthèse en français ou en arabe |
| Vérifier la demande ? | Le publier comme contenu gratuit d'acquisition pour les produits 1 et 4, et mesurer les demandes de version payante |

Révision : profit 8 → 6, validation 9 → 8, défendabilité 4 → 2, acquisition 5 → 4.

**6. Veille réglementaire pharma Maroc (#61) — 57 → 47**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Le mandant vendrait à ses pairs et aux concurrents de son employeur une lecture du même régulateur |
| Saturé ? | Non : aucun traqueur AMMPS structuré en français ou en anglais n'a été trouvé |
| Concurrents mieux financés ? | Cortellis et AgencyIQ, sans profondeur marocaine |
| Pourquoi pas ChatGPT ou Claude ? | Sources locales peu lisibles par machine : bonne défense |
| Automatisation difficile ? | La vérification des échéances réglementaires, qui exige un contrôle humain expert |
| Coût destructeur ? | Le coût n'est pas financier : c'est l'emploi principal. La divulgation de secrets professionnels figure parmi les fautes graves citées au titre de l'article 39 du Code du travail [S, cabinet] ([CMS](https://cms.law/en/mar/legal-updates/ce-qu-il-faut-savoir-sur-le-licenciement-pour-faute-grave-au-maroc)) |
| Hypothèse fragile ? | Que l'employeur autorise par écrit, et qu'un client distingue « donnée publique » d'« initié du secteur » |
| Vérifier la demande ? | Seulement après autorisation écrite ; sinon ne pas tester |

Révision forte : profit 12 → 9 (univers de 50 à 60 laboratoires), validation 8 → 5, acquisition 6 → 3, Maroc 2 → 1.

**7. Veille d'appels d'offres + mémoire technique France (#13) — 57 → 50**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Jorpex, Palmio, Explain, Olra occupent le terrain ; un actor Apify BOAMP + TED existe déjà ([Apify](https://apify.com/tagadanar/french-public-tenders)) |
| Saturé ? | Oui pour la veille ; en cours de saturation pour la rédaction |
| Concurrents mieux financés ? | Oui |
| Pourquoi pas ChatGPT ou Claude ? | La rédaction du mémoire à partir du dossier de consultation est exactement ce qu'un assistant fait avec les documents du client |
| Automatisation difficile ? | La rédaction (50–70 % automatisable [H]) exige la base de connaissances du client, donc ses documents confidentiels |
| Coût destructeur ? | Le support de rédaction, qui redevient un service |
| Hypothèse fragile ? | Qu'un nouvel entrant marocain se différencie par le prix sous l'ancre de 49 USD |
| Vérifier la demande ? | Échantillon « trois appels d'offres manqués le mois dernier » envoyé à de petits lots de PME d'un seul métier |

Révision : profit 10 → 8, autonomie 14 → 13, validation 9 → 8, défendabilité 3 → 2, acquisition 5 → 3.

**8. App Shopify (#24) — 56 → 49**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Revenu médian du premier trimestre de 0 USD sur ~700 nouvelles apps (donnée de 2021 recyclée) [S] ([Barn2](https://barn2.com/blog/shopify-app-store-saturation/)) |
| Saturé ? | 21 509 apps publiques, 2 713 lancées en un mois [S] |
| Concurrents mieux financés ? | Les 16 plus grosses apps capteraient 40 % du revenu [S, attribution non vérifiée] |
| Pourquoi pas ChatGPT ou Claude ? | L'intégration dans la boutique protège ; c'est le point fort |
| Automatisation difficile ? | Le support marchand et les réponses aux avis : c'est de l'exploitation |
| Coût destructeur ? | Le temps humain de support ; la dépendance aux règles de la plateforme |
| Hypothèse fragile ? | Que le versement partenaire atteigne le Maroc (aucun document ne le nomme) |
| Vérifier la demande ? | Vélocité des avis et prix des concurrents sur la catégorie visée |

Révision : profit 10 → 7, autonomie 13 → 12, acquisition 6 → 4, Maroc 5 → 4.

**9. App Atlassian Forge (#25) — 56 → 51**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Aucune donnée de revenu solo n'a été trouvée ; l'incitation à 0 % est qualifiée de temporaire par Atlassian |
| Saturé ? | Moins que les magasins grand public [H chercheurs] |
| Concurrents mieux financés ? | Éditeurs d'add-ons établis |
| Pourquoi pas ChatGPT ou Claude ? | L'intégration dans Jira / Confluence protège |
| Automatisation difficile ? | Contraintes de la plateforme Forge et revue de sécurité |
| Coût destructeur ? | Le délai : la construction et la revue repoussent la première recette |
| Hypothèse fragile ? | Versement vers le Maroc non confirmé |
| Vérifier la demande ? | Lecture des avis et demandes non satisfaites sur la place de marché |

Révision : profit 11 → 10, autonomie 13 → 12, validation 6 → 4, Maroc 5 → 4.

**10. Intelligence réglementaire panafricaine (#62) — 55 → 50**

| Question | Réponse |
|---|---|
| Pourquoi échouer ? | Les sources nationales sont des PDF dispersés ; la couverture promise devient vite un travail manuel |
| Saturé ? | Non au niveau de prix visé |
| Concurrents mieux financés ? | Cortellis, RegASK, Freyr (prix non publics) |
| Pourquoi pas ChatGPT ou Claude ? | Bonne défense : données non récupérables à la demande |
| Automatisation difficile ? | 30–40 % du travail récurrent selon les chercheurs |
| Coût destructeur ? | Le temps d'expert pour valider |
| Hypothèse fragile ? | Que des cabinets de conseil acceptent de revendre : recruter des partenaires, c'est vendre |
| Vérifier la demande ? | Une fiche pays vendue à l'unité avant tout abonnement |

Révision : autonomie 12 → 10, validation 6 → 5, acquisition 4 → 3, Maroc 5 → 4.

### Scores révisés et nouveau classement

| Rang révisé | Opportunité | Score initial | Score révisé | Écart | Raison dominante |
|---|---|---|---|---|---|
| 1 | Radar AO santé bailleurs Afrique (#64) | 66 | **60** | −6 | Acquisition sans appels non prouvée ; conditions des portails non lues |
| 2 | Veille cosmétiques / compléments (#73) | 61 | **58** | −3 | Demande non prouvée, mais meilleur profil COI et pas de concurrence frontale |
| 3 | Actors Apify (#6) | 64 | **56** | −8 | Revenus concentrés, commodité au centime, versement non confirmé |
| 4 | Alertes TED santé / medtech (#65) | 62 | **54** | −8 | Marché banalisé, bande de prix à rétention de 23 % |
| 5 | Digest inspections GMP (#68) | 58 | **52** | −6 | Substituable par un assistant |
| 6 | App Atlassian Forge (#25) | 56 | 51 | −5 | Délai et versement non confirmé |
| 7 | Veille AO + mémoire France (#13) | 57 | 50 | −7 | Saturation |
| 8 | Intelligence réglementaire panafricaine (#62) | 55 | 50 | −5 | Automatisation partielle |
| 9 | App Shopify (#24) | 56 | 49 | −7 | Médiane à zéro, support |
| 10 | Veille réglementaire pharma Maroc (#61) | 57 | 47 | −10 | Conflit d'intérêts avec l'employeur |

La contre-expertise retire en moyenne 6,5 points au top 10. Les rangs 11 à 20 n'ont pas subi la seconde passe : leurs scores initiaux (47 à 53) ne sont donc pas comparables aux scores révisés, et la même décote moyenne les placerait tous sous 47. Deux mouvements comptent. La veille pharma Maroc, qui exploite le mieux l'expertise du mandant, passe de la sixième à la dixième place : **l'avantage d'expertise est exactement ce qui crée le conflit d'intérêts**. Apify cède la deuxième place à la veille cosmétiques/compléments parce que la distribution intégrée ne compense pas un revenu attendu proche de zéro. Aucun score révisé ne dépasse 60 sur 100 : la sélection désigne les moins mauvais paris, pas des paris sûrs.


---

## E. Top 5 deep-dive — cinq produits, un seul pipeline, des scénarios qui restent modestes

### Règles de calcul communes aux cinq fiches

Les formules sont identiques partout. **Marge sur coûts variables unitaire** = revenu net encaissé par unité − coûts variables unitaires. **Résultat d'exploitation** = chiffre d'affaires hors taxes − coûts variables − coûts fixes d'exploitation. **Seuil de rentabilité** = coûts fixes ÷ marge unitaire. **ROI** = (gain net cumulé − investissement initial) ÷ investissement initial, à l'horizon indiqué.

Les faits de coût sont vérifiés : le marchand officiel prélève 5 % + 0,50 USD par transaction chez Paddle comme chez Lemon Squeezy [F] ([Paddle](https://www.paddle.com/pricing), [Lemon Squeezy](https://www.lemonsqueezy.com/pricing)) ; les prix Claude par million de jetons sont de 0,10 / 0,50 USD (Haiku 5.5), 2 / 10 USD (Sonnet 5.5), 4 / 20 USD (Opus 5.5) et 8 / 40 USD (Fable 5.2) en entrée / sortie, avec 50 % de remise en traitement par lots [F] ([Anthropic, tarifs](https://platform.claude.com/docs/en/about-claude/pricing)). Tout le reste est hypothèse [H] : nombre de clients, prix retenu, provision de 3 % pour remboursements, volumes de jetons (non mesurés ; les chercheurs recommandent de compter les jetons sur des échantillons réels avant de figer un budget), budget d'outils d'acquisition de 30 USD par mois.

Quatre avertissements valent pour tous les tableaux. Les nombres de clients sont **nets d'attrition** et sont des hypothèses de scénario, pas des prévisions ; le scénario favorable correspond au sommet de la distribution observée et **n'est pas une prévision**. Le repère de planification des chercheurs pour un produit lancé est de 0 à 200 USD de MRR après six mois ; notre scénario prudent s'y conforme, le scénario central le dépasse déjà. Le résultat est donné **avant impôt de l'exploitant** : l'impôt dépend du statut non encore choisi (1 % des encaissements en auto-entrepreneur de services ; environ 29 % du bénéfice distribué en SARL AU en 2026, taux à confirmer). Enfin, deux bases de coûts fixes sont montrées : « hors structure » et « avec SARL AU » à 20 000 MAD par an, soit ~167 USD par mois, hypothèse basse-moyenne de la fourchette de 15 000 à 50 000 MAD citée par des cabinets [S] ([ClicPaie](https://clicpaie.ma/blogs/creer-sarl-maroc/)). Le ROI est mécaniquement spectaculaire dans les scénarios positifs parce que le capital engagé est minuscule : la ressource rare est le client, pas le capital.

Les cinq produits partagent la même chaîne (collecter → filtrer → résumer → livrer). Si le portefeuille tourne sur une infrastructure commune, les coûts fixes ne s'additionnent pas : l'estimation est de 220 à 280 USD par mois pour trois produits au lieu de 360 [E].

---

### E.1 Radar d'appels d'offres santé des bailleurs en Afrique (#64) — score révisé 60

| Rubrique | Contenu |
|---|---|
| Concept exact | Abonnement B2B. Chaque jour ouvré, le pipeline relève les avis d'appels d'offres de produits de santé publiés par les portails des bailleurs et des agences (UNGM, Banque mondiale, BAD, Fonds mondial, UNICEF Supply Division, centrales d'achat nationales) et par TED, les filtre, les apparie au profil du client (DCI, formes, classes de dispositifs, pays, préqualification OMS) et envoie une alerte résumée en français ou en anglais avec le lien vers l'avis source. Le produit stocke des métadonnées et des liens, ne republie pas les dossiers et n'héberge aucune donnée client au-delà du compte et de la facturation |
| Client cible | Exportateurs et distributeurs de génériques, dispositifs et consommables ; fournisseurs d'ONG ; PME d'Inde, de Tunisie, d'Égypte, d'Europe et du Maroc. **Exclusion de principe : tout appel d'offres, pays ou produit sur lequel l'employeur du mandant soumissionne** |
| Problème résolu | Les avis sont dispersés sur des portails hétérogènes ; un avis manqué est une vente perdue |
| Proposition de valeur | Moins d'avis, mieux triés, par molécule ; responsabilité assumée sur la complétude du périmètre annoncé |
| Preuve de marché disponible | Concurrents à prix publics : Open Opportunities 160–342 USD/mois [F] ([OpenOpps](https://www.openopps.com/pricing)), Jorpex 49–149 USD/mois [S] ([Jorpex](https://jorpex.com/compare/tender-monitoring-tools/)), L2B « Daily Tenders Africa » 1 721,74 ZAR hors TVA, période non confirmée [S] ([L2B](https://www.l2b.co.za/Tenders/Tender-Pricing)). Contexte : l'Afrique subsaharienne importe plus de 70 % de ses médicaments [F] ([IFC](https://www.ifc.org/en/stories/2025/answering-africas-call-for-private-investment-in-pharma-manufacturing)). **Aucun revenu d'opérateur solo vérifié dans cette niche** |
| Concurrents | Généralistes : Open Opportunities, TendersOnTime, Tendersinfo, GlobalTenders, L2B ; alertes gratuites des portails eux-mêmes ; actors Apify à 10 USD/mois |
| Prix envisagés et justification | 99 USD/mois (un profil), 149 USD/mois (équipe, multi-zones, historique), annuel à dix mois [H]. Sous l'offre Solo d'Open Opportunities, dans la bande 50–249 USD où la rétention brute médiane est de 45 %, avec incitation à l'annuel qui ajoute 10 à 20 points de rétention nette [F] ([ChartMogul](https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/)) |
| Tunnel de vente | Pages publiques par catégorie d'appels d'offres (la page est la surface du produit) ; échantillon personnalisé « trois avis que vous avez manqués le mois dernier » envoyé par petits lots de moins de 50 destinataires, régime où l'e-mail fonctionne encore (5,8 % de réponses contre 2,1 % au-delà de 500) [S, fournisseur] ([Woodpecker citant Belkins](https://woodpecker.co/blog/cold-email-statistics/%20)) ; essai puis paiement par le marchand officiel. Aucun envoi vers des contacts marocains sans consentement préalable ; règles de prospection B2B à vérifier pays par pays dans l'UE |

**Scénarios financiers (USD par mois à l'échéance ; hypothèses : prix 99 USD ; frais du marchand officiel 5,45 USD ; IA marginale 2 USD par client ; provision remboursements 2,97 USD ; marge unitaire 88,58 USD ; coûts fixes 140 USD hors structure).**

| Scénario | Échéance | Clients nets [H] | Chiffre d'affaires | Coûts variables | Coûts fixes | Résultat d'exploitation |
|---|---|---|---|---|---|---|
| Prudent | 3 mois | 0 | 0 | 0 | 140 | −140 |
| Prudent | 6 mois | 1 | 99 | 10 | 140 | −51 |
| Prudent | 12 mois | 3 | 297 | 31 | 140 | +126 |
| Central | 3 mois | 2 | 198 | 21 | 140 | +37 |
| Central | 6 mois | 5 | 495 | 52 | 140 | +303 |
| Central | 12 mois | 12 | 1 188 | 125 | 140 | +923 |
| Favorable (non prévisionnel) | 3 mois | 5 | 495 | 52 | 140 | +303 |
| Favorable (non prévisionnel) | 6 mois | 15 | 1 485 | 156 | 140 | +1 189 |
| Favorable (non prévisionnel) | 12 mois | 40 | 3 960 | 417 | 140 | +3 403 |

| Indicateur [E] | Prudent | Central | Favorable |
|---|---|---|---|
| Résultat cumulé sur 12 mois, hors structure (interpolation linéaire entre échéances) | −351 USD | +4 565 USD | +18 029 USD |
| Idem avec SARL AU (−2 004 USD/an) | −2 355 USD | +2 561 USD | +16 025 USD |
| ROI à 12 mois sur 400 USD d'investissement initial [H], hors structure | −188 % | +1 041 % | +4 407 % |
| Besoin de trésorerie maximal (investissement + pertes cumulées) | ~1 085 USD | ~503 USD | ~400 USD |
| Seuil de rentabilité | 2 clients hors structure (140 ÷ 88,58 = 1,6) ; 4 clients avec SARL AU (307 ÷ 88,58 = 3,5) | | |
| Délai jusqu'au premier revenu [H] | 6 à 10 semaines après autorisation de la Phase 2 ; non atteint à 3 mois dans le scénario prudent | | |

Le scénario favorable cumulerait environ 22 000 USD d'encaissements sur douze mois, soit plus que le plafond de 200 000 MAD par an du statut d'auto-entrepreneur de services [F] ([Loi 114-13](https://adala.justice.gov.ma/api/uploads/2024/05/07/Loi%20Relative%20au%20statut%20de%20l%E2%80%99auto-entrepreneur-1715071318209.pdf)).

**Coûts d'exploitation mensuels.**

| Poste | Montant | Nature |
|---|---|---|
| API IA du pipeline (Haiku 5.5 pour classer, Sonnet 5.5 en lots pour résumer) | ~40 USD | [E] Le cas de référence des chercheurs, 5 000 avis par jour, coûte 83 à 166 USD/mois ; le volume réel de cette niche n'est pas connu et un préfiltre par code le réduit fortement |
| Revue stratégique hebdomadaire Fable 5.2 | ~10 USD | [E] Une tâche de recherche approfondie coûte 1,49 à 4,82 USD selon l'effort [F] ([Anthropic](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)) |
| Hébergement, base de données, e-mail transactionnel | ~50 USD | [E] Socle de 35 à 125 USD/mois : VPS, Postgres, Resend, Workers |
| Outils d'acquisition (domaine d'envoi, boîtes, données) | ~30 USD | [H] |
| Divers (domaine, surveillance) | ~10 USD | [H] |
| Frais du marchand officiel | 5 % + 0,50 USD par vente | [F] |
| Support et contrôle qualité | ~0,02 USD par e-mail traité en Sonnet 5.5 [E] ; le coût réel est le temps du mandant | |
| Remboursements | 3 % du chiffre d'affaires | [H] |
| Structure juridique | 0 (auto-entrepreneur, hors cotisations non vérifiées) ou ~167 USD (SARL AU) | [S] |

**Système agentique requis.**

| Étape | Agent responsable | Outils | Déclencheur | Données | Actions | Niveau | Contrôles qualité | Coût | Risque de défaillance | Procédure de reprise |
|---|---|---|---|---|---|---|---|---|---|---|
| Veille de marché | Stratège (Fable 5.2, effort bas ou moyen) | Recherche web, base interne | Cron hebdomadaire | Prix concurrents, nouvelles sources, métriques | Note de synthèse, propositions chiffrées | C | Citations obligatoires, liens testés par code | 1,5–5 USD par note | Biais, affirmations fausses | Le mandant tranche ; relance avec consigne corrigée |
| Création du produit | Constructeur (Claude Code sans interface, Opus 5.5 ou Sonnet 5.5) | Dépôt Git, tests, budget plafonné par exécution | Ticket approuvé | Spécifications, jeu d'or de 50 avis vérifiés à la main | Connecteurs de sources, schéma, validateurs | C | Tests automatiques, revue du diff, mise en production approuvée | ~0,84 USD par tentative de codage sur Opus 5.5 [F] | Régression | Retour arrière Git |
| Publication (collecte et alertes) | Chaîne Collecteur → Classifieur (Haiku 5.5) → Rédacteur (Sonnet 5.5, lots) | Cron, file Postgres, flux et API officiels | Quotidien | Avis publics | Collecte, préfiltre par code, classement, résumé, envoi | B | Validation de schéma, liens vivants, rapprochement des volumes avec la source, échantillon de 5 % revu, alerte si volume anormal | ~40 USD/mois | Portail modifié, avis manqué | Reprise idempotente, alerte « source cassée », ticket au Constructeur |
| Acquisition | Prospection (Sonnet 5.5) | Liste issue de sources publiques, outil d'envoi | **Lot approuvé par le mandant** | Sociétés, catégories d'intérêt | Échantillon personnalisé, séquence courte | C | Liste d'exclusion (employeur, Maroc sans consentement, pays à consentement), plafond d'envoi, lien de désinscription | ~30 USD/mois + centimes | Réputation du domaine, plainte | Suspension automatique si rebonds > 2 % ou plainte |
| Conversion | Page d'offre + agent de réponse | Site, essai, brouillons d'e-mail | Réponse entrante | Historique du prospect | Réponse factuelle, lien d'essai | B (réponses types), C (toute concession) | Mention « assistant IA », aucun pouvoir de remise | Centimes | Promesse fausse au prospect | Brouillon en file d'approbation |
| Paiement | Marchand officiel | Checkout, TVA, factures | Achat | Aucune donnée carte chez le vendeur | Encaissement, virement vers la banque marocaine | A (encaissement), **D (ouverture de compte, KYC, déclarations)** | Rapprochement mensuel par code | 5 % + 0,50 USD | Gel de compte, retard de versement | Seconde voie d'encaissement approuvée à l'avance ; balayage des soldes |
| Livraison | Chaîne de publication | Resend, tableau client | Quotidien / hebdomadaire | Profil client | Alerte, digest | A | Taux de délivrabilité, contrôle « zéro alerte anormale » | Inclus | Envoi vide ou en double | Clé d'idempotence |
| Support | Support (Haiku 5.5 pour trier, Sonnet 5.5 pour rédiger) | Boîte partagée, base de connaissances | E-mail entrant | Compte, historique | Réponse aux questions courantes | B ; C pour remboursement, litige, réclamation | Aucun outil d'argent, plafond de remboursement codé en dur | ~0,02 USD par e-mail | Complaisance, injection d'instructions | Escalade au mandant ; gel du compte concerné |
| Rétention | Chaîne de reporting client | Base, e-mail | Mensuel | Avis envoyés, ouverts, pertinents | Rapport de valeur, offre annuelle | B | Chiffres recalculés par code | Centimes | Rapport erroné | Rectificatif |
| Optimisation | Stratège | Métriques | Mensuel | Attrition, conversion, coût IA | Propositions de prix, de sources, de coupes | C | Seuils de la section G | Inclus | Sur-optimisation | Décision du mandant |
| Reporting | Tableau de bord (code) + synthèse Fable | Exports du marchand officiel, journaux | Hebdomadaire | Recettes, coûts, incidents | Rapport d'une page | A | Totaux rapprochés | Inclus | Donnée manquante | Alerte |

**Part automatisable, temps humain et criticité.** En volume de tâches, 90 à 95 % des opérations récurrentes sont exécutées sans intervention (des milliers de classements contre quelques dizaines de décisions) [E] ; les chercheurs estiment à 80–90 % la part du travail récurrent automatisable [H]. Le temps résiduel du mandant est de 4 à 6 heures par semaine pendant six à huit semaines de mise en place, puis de **2 à 3 heures par semaine** [H]. Les interventions à criticité élevée sont : autorisation de l'employeur, contrats et KYC, approbation de chaque lot de prospection, remboursements et litiges, ajout d'une source dont les conditions n'ont pas été lues. Le modèle n'est donc pas « 100 % autonome ».

**Difficultés, risques, leviers, validation.** La difficulté concrète est le rappel : prouver qu'aucun avis du périmètre n'est manqué, portail par portail. Les risques sont, par ordre de gravité : conditions de réutilisation des portails des bailleurs non vérifiées ; recouvrement avec les marchés de l'employeur ; acquisition nulle ; gel de compte chez le marchand officiel. Les leviers de croissance sont l'historique des attributions et des prix, l'extension par zone, le palier équipe, et la revente de l'actor de collecte sur Apify. La validation suit la section I : source TED d'abord, lecture des conditions des portails, digest concierge gratuit, puis pilotes payés.

---

### E.2 Veille de conformité cosmétiques et compléments alimentaires (#73) — score révisé 58

| Rubrique | Contenu |
|---|---|
| Concept exact | Bulletin hebdomadaire, alertes et base consultable sur les textes et décisions applicables aux cosmétiques et aux compléments alimentaires au Maroc, dans l'UE et dans le Golfe : AMMPS, ONSSA, Bulletin officiel, bases européennes CosIng et Novel Food. Chaque entrée renvoie au texte officiel. Positionnement : information, pas conseil réglementaire |
| Client cible | Petites marques, importateurs et distributeurs ; consultants en affaires réglementaires et cabinets, qui sont les clients les plus accessibles (pas de qualification fournisseur, paiement par carte) [H chercheurs] |
| Problème résolu | Régime marocain contesté en 2026 : enregistrement préalable AMMPS selon l'ONSSA contre lecture de la loi 28-07 par la filière ; amendement réservant aux pharmacies les compléments « à effet thérapeutique » adopté par la première chambre en juin 2026 [S presse] ([TelQuel](https://telquel.ma/instant-t/2026/06/11/le-secteur-des-complements-alimentaires-soppose-au-monopole-des-pharmacies_1993544/), [Médias24](https://medias24.com/2026/04/15/enquete-complements-alimentaires-dans-les-coulisses-dun-marche-bien-insuffisamment-regule-1659623/)) |
| Proposition de valeur | « Ce qui a changé, ce que cela implique, pour quand », avec le texte source, en français et en anglais |
| Preuve de marché disponible | **Indirecte seulement.** Aucun concurrent tarifé identifié ; budget de substitution : consultants réglementaires à 40–150 USD/h [S] ([Kolabtree](https://www.kolabtree.com/find-an-expert/subject/regulatory-affairs)) ; petits outils voisins à 69–119 USD/mois [S] ([Capterra](https://www.capterra.com/p/10049639/Pharmatext/), [GetApp](https://www.getapp.com/all-software/a/bibliovigilance/)). Le nombre de marques et d'importateurs n'a pas été dénombré |
| Concurrents | Presse professionnelle, cabinets de conseil, associations ; assistants généralistes |
| Prix envisagés et justification | 79 USD/mois ou 790 USD/an ; palier cabinet à 149 USD/mois [H]. Milieu de la fourchette de 50–200 USD/mois inférée par les chercheurs ; au-dessus de 50 USD pour sortir de la bande de rétention à 23 % |
| Tunnel de vente | Trois numéros gratuits sur la réforme en cours, inscription volontaire, relais par les associations professionnelles, puis prévente annuelle. Au Maroc, la prospection par e-mail exige le consentement préalable sans exception B2B [F] ([CNDP](https://www.cndp.ma/wp-content/uploads/2025/07/fiche_CNDP_Prospection_RT_fr.pdf)) : l'acquisition locale est entrante |
| Conflit d'intérêts | Faible à moyen, **sauf si l'employeur vend des compléments ou des dermo-cosmétiques** : à vérifier avant tout |

**Scénarios financiers (prix 79 USD ; frais du marchand officiel 4,45 USD ; IA marginale 1,50 USD ; provision remboursements 2,37 USD ; marge unitaire 70,68 USD ; coûts fixes 120 USD hors structure).**

| Scénario | Échéance | Clients nets [H] | Chiffre d'affaires | Coûts variables | Coûts fixes | Résultat d'exploitation |
|---|---|---|---|---|---|---|
| Prudent | 3 mois | 0 | 0 | 0 | 120 | −120 |
| Prudent | 6 mois | 1 | 79 | 8 | 120 | −49 |
| Prudent | 12 mois | 2 | 158 | 17 | 120 | +21 |
| Central | 3 mois | 2 | 158 | 17 | 120 | +21 |
| Central | 6 mois | 4 | 316 | 33 | 120 | +163 |
| Central | 12 mois | 10 | 790 | 83 | 120 | +587 |
| Favorable (non prévisionnel) | 3 mois | 5 | 395 | 42 | 120 | +233 |
| Favorable (non prévisionnel) | 6 mois | 12 | 948 | 100 | 120 | +728 |
| Favorable (non prévisionnel) | 12 mois | 30 | 2 370 | 250 | 120 | +2 000 |

| Indicateur [E] | Prudent | Central | Favorable |
|---|---|---|---|
| Résultat cumulé sur 12 mois, hors structure | −627 USD | +2 730 USD | +10 858 USD |
| Idem avec SARL AU | −2 631 USD | +726 USD | +8 854 USD |
| ROI à 12 mois sur 400 USD [H], hors structure | −257 % | +583 % | +2 615 % |
| Besoin de trésorerie maximal | ~1 058 USD | ~499 USD | ~402 USD |
| Seuil de rentabilité | 2 clients hors structure (120 ÷ 70,68 = 1,7) ; 5 clients avec SARL AU (287 ÷ 70,68 = 4,1) | | |
| Délai jusqu'au premier revenu [H] | 8 à 12 semaines ; la médiane des newsletters lancées en 2025 sur beehiiv est de 66 jours jusqu'au premier dollar [F] ([beehiiv](https://www.beehiiv.com/blog/the-state-of-newsletters-2026)) | | |

Les clients marocains paieraient vraisemblablement par virement ou par un agrégateur local (Payzone, YouCan Pay), dont les tarifs n'ont pas été vérifiés [I] ; une SARL facturerait 20 % de TVA aux clients marocains alors qu'un auto-entrepreneur est hors champ [S] ([Le Matin](https://lematin.ma/economie/auto-entrepreneur-ce-que-prevoit-le-regime-fiscal-en-2026/361537)).

**Coûts d'exploitation mensuels.** API IA ~20 USD (une vingtaine de sources hebdomadaires : un bulletin coûte 0,36 à 0,80 USD en chaîne Haiku puis Sonnet ou Fable [E]) ; revue Fable ~10 USD ; hébergement et e-mail ~50 USD ; acquisition ~30 USD [H] ; divers ~10 USD ; marchand officiel 5 % + 0,50 USD ; remboursements 3 % [H] ; structure 0 ou ~167 USD.

**Système agentique requis.**

| Étape | Agent responsable | Outils | Déclencheur | Données | Actions | Niveau | Contrôles qualité | Coût | Risque de défaillance | Procédure de reprise |
|---|---|---|---|---|---|---|---|---|---|---|
| Veille de marché | Stratège (Fable 5.2) | Recherche web | Mensuel | Calendrier législatif, concurrents | Note, sujets prioritaires | C | Sources citées | 1,5–5 USD | Lecture erronée d'un projet de texte | Arbitrage du mandant |
| Création du produit | Constructeur (Claude Code) | Git, tests | Ticket approuvé | Gabarit de fiche, liste de sources | Collecteurs, modèle de fiche | C | Tests, mise en production approuvée | Plafond par exécution | Source PDF mal lue | Correctif, retour arrière |
| Publication | Collecteur → Classifieur (Haiku 5.5) → Rédacteur (Sonnet 5.5) → Vérificateur (code + second passage) | Cron, récupération web, lecture PDF | Quotidien (collecte), hebdomadaire (bulletin) | Textes officiels publics | Détection de nouveautés, fiche « quoi / pour qui / quand », lien source | **B avec contrôle renforcé : toute échéance réglementaire citée est revue par échantillonnage par le mandant** | Citation textuelle de l'article, lien vivant, avertissement « information, pas conseil » | ~20 USD/mois | Échéance fausse : le risque le plus grave | Rectificatif à tous les abonnés, journal des corrections |
| Acquisition | Rédacteur de contenu + formulaire d'inscription | Site, numéros gratuits | Publication | Inscriptions volontaires | Diffusion aux inscrits, relais associatifs | C (tout partenariat est décidé par le mandant) | Preuve de consentement conservée | ~30 USD/mois | Liste trop petite | Changer de canal avant d'augmenter la dépense |
| Conversion | Page de prévente annuelle | Site, marchand officiel | Fin de la série gratuite | Engagement des lecteurs | Offre fondateur | B | Aucune fausse rareté, aucun témoignage inventé | Centimes | Zéro prévente | Critère d'abandon (section I) |
| Paiement | Marchand officiel ; virement pour clients marocains | Checkout, facture | Achat | — | Encaissement | A ; D pour comptes et déclarations | Rapprochement | 5 % + 0,50 USD | Friction de paiement locale | Facture + virement |
| Livraison | Chaîne de publication | E-mail, base consultable | Hebdomadaire | Profil | Bulletin, alertes | A | Délivrabilité | Inclus | Envoi manqué | Reprise idempotente |
| Support | Support (Haiku 5.5 + Sonnet 5.5) | Boîte partagée | E-mail entrant | Historique | Réponses sur le service | B ; **C pour toute question « que dois-je faire dans mon cas », renvoyée vers un professionnel** | Refus codé du conseil individuel | ~0,02 USD par e-mail | Glissement vers le conseil | Escalade |
| Rétention | Reporting client | Base | Mensuel | Textes couverts | Récapitulatif, renouvellement annuel | B | Recalcul par code | Centimes | — | — |
| Optimisation | Stratège | Métriques | Mensuel | Ouvertures, attrition | Propositions | C | Seuils section G | Inclus | — | Décision du mandant |
| Reporting | Tableau de bord | Exports | Hebdomadaire | Recettes, coûts | Rapport | A | Rapprochement | Inclus | — | Alerte |

**Part automatisable, temps humain et criticité.** Environ 85 à 90 % des tâches récurrentes en volume [E] ; 75 % du travail récurrent selon les chercheurs [H]. Temps résiduel : **2 à 4 heures par semaine** [H], plus élevé que pour le radar parce que l'échantillonnage des échéances réglementaires demande l'œil d'un expert. C'est le seul des cinq produits où l'expertise du mandant sert directement sans exposer de données de l'employeur, à condition que seules des sources publiques alimentent le produit, avec un journal de source par donnée.

**Difficultés, risques, leviers, validation.** Difficulté : des sources marocaines peu structurées et un droit en mouvement. Risques : erreur sur une échéance, glissement vers le conseil, marché local trop petit ou réticent au paiement par carte, recouvrement avec les gammes de l'employeur. Leviers : extension aux dispositifs médicaux (#74, COI faible à moyen si l'employeur ne vend que des médicaments), versions Golfe et UE vendues à des exportateurs, palier cabinet. Validation : trois numéros gratuits, au moins 100 inscriptions volontaires qualifiées, puis prévente annuelle.


---

### E.3 Scrapers « Actors » sur Apify Store (#6) — score révisé 56

| Rubrique | Contenu |
|---|---|
| Concept exact | Cinq à dix actors publiés sur Apify Store, chacun exposant en données structurées une source publique dont la réutilisation est vérifiée (TED, openFDA, pages de l'EMA) ou une source francophone ou africaine mal couverte, après lecture de ses conditions. Tarification à l'événement. Ce sont les collecteurs des produits E.1 et E.2, publiés une seconde fois comme produits autonomes |
| Client cible | Développeurs, agences de données, agents IA qui consomment des outils (les actors exposent déjà un accès MCP) |
| Problème résolu | Obtenir des données structurées sans écrire ni maintenir le collecteur |
| Proposition de valeur | Un collecteur entretenu, à l'usage, facturé par la plateforme |
| Preuve de marché disponible | Apify déclare avoir versé plus de 563 000 USD aux développeurs en septembre 2025 et plus de 4 millions au total [S, communiqué] ([NatLawReview](https://natlawreview.com/press-releases/apify-bets-1m-independent-developers-building-ais-missing-tools)) ; la tarification à l'événement représente 87 % de la demande [S] ([SignalCensus](https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau)). Contre-preuve : 0 USD de revenu malgré 5 407 résultats livrés dans un cas [AD]. **Aucune distribution des revenus par créateur n'est publiée** |
| Concurrents | 25 787 actors ; sur les appels d'offres, des actors à 10 USD/mois ou 0,10 USD les 1 000 résultats |
| Prix envisagés et justification | Tarification à l'événement alignée sur les actors voisins ; le créateur garde 80 % moins le coût de calcul [S, doc officielle] ([Apify](https://docs.apify.com/actors/monetize.md)). Le modèle locatif a été retiré le 1er octobre 2026 |
| Tunnel de vente | Recherche interne à la place de marché ; aucune prospection. C'est le seul des cinq produits qui ne demande ni e-mail ni appel |

**Scénarios financiers.** Le revenu dépend d'un volume d'usage que rien ne permet de prévoir : **le scénario central n'est pas estimable de façon fiable**, et les chiffres ci-dessous sont des hypothèses d'illustration. Hypothèses : part créateur 80 % ; calcul de plateforme 15 % du brut [H] ; frais de retrait et de change 4 % du net [H, d'après les 3–4 % rapportés pour PayPal Maroc] ; soit 62,4 % du brut encaissé ; coûts fixes 30 USD par mois (jetons de maintenance et surveillance) ; investissement initial 150 USD [H].

| Scénario | Échéance | Usage brut facturé [H] | Net encaissé | Coûts fixes | Résultat d'exploitation |
|---|---|---|---|---|---|
| Prudent | 3 mois | 0 | 0 | 30 | −30 |
| Prudent | 6 mois | 10 | 6 | 30 | −24 |
| Prudent | 12 mois | 30 | 19 | 30 | −11 |
| Central (illustratif) | 3 mois | 30 | 19 | 30 | −11 |
| Central (illustratif) | 6 mois | 100 | 62 | 30 | +32 |
| Central (illustratif) | 12 mois | 300 | 187 | 30 | +157 |
| Favorable (non prévisionnel) | 3 mois | 200 | 125 | 30 | +95 |
| Favorable (non prévisionnel) | 6 mois | 800 | 499 | 30 | +469 |
| Favorable (non prévisionnel) | 12 mois | 2 500 | 1 560 | 30 | +1 530 |

| Indicateur [E] | Prudent | Central (illustratif) | Favorable |
|---|---|---|---|
| Résultat cumulé sur 12 mois | −266 USD | +632 USD | +7 721 USD |
| ROI à 12 mois sur 150 USD | −278 % | +321 % | +5 047 % |
| Besoin de trésorerie maximal | ~416 USD | ~203 USD | ~150 USD |
| Seuil de rentabilité | ~48 USD d'usage brut par mois (30 ÷ 0,624) | | |
| Délai jusqu'au premier revenu [H] | 4 à 8 semaines si l'actor trouve des utilisateurs payants ; factures générées le 11 de chaque mois, versement minimal de 20 USD par PayPal [S] ([Apify](https://docs.apify.com/actors/publishing/monetize/monthly-payouts.md)) | | |

Le scénario favorable reste en deçà du seuil de 10 000 USD de MRR que l'aide d'Apify attribue à ses meilleurs créateurs indépendants (page ancienne, modèle locatif) [S] ([Apify](https://help.apify.com/en/articles/8684010-how-does-actor-monetization-work)).

**Coûts d'exploitation.** Jetons de maintenance ~20 USD/mois [E] ; surveillance ~10 USD ; aucune dépense d'acquisition ; commission de plateforme 20 % et calcul déduits à la source ; retrait PayPal vers une banque marocaine gratuit au-dessus de 2 000 MAD, 30 MAD en dessous, hors change [S, blog fournisseur] ([Grey](https://grey.co/blog/wise-vs-paypal-vs-payoneer-which-works-better-for-moroccans)).

**Système agentique requis.**

| Étape | Agent responsable | Outils | Déclencheur | Données | Actions | Niveau | Contrôles qualité | Coût | Risque de défaillance | Procédure de reprise |
|---|---|---|---|---|---|---|---|---|---|---|
| Veille de marché | Stratège (Opus 5.5 suffit) | Recherche sur la place de marché | Mensuel | Catégories, concurrents, prix | Liste de sources candidates | C | Lecture des conditions de chaque source avant tout développement | ~1 USD | Choix d'une source interdite | Refus par défaut si conditions non lues |
| Création du produit | Constructeur (Claude Code) | SDK Apify, tests | Source approuvée | Schéma de sortie | Actor, documentation | C (publication approuvée) | Tests sur échantillon, pas de contournement anti-robot | ~0,84 USD par tentative | Collecteur fragile | Correctif |
| Publication | Constructeur | Console Apify | Approbation | Fiche, prix | Mise en ligne | C | Fiche exacte, pas de promesse de couverture non tenue | — | Rejet | Correction |
| Acquisition | Place de marché | Recherche interne | Continu | — | Aucune | A | — | 0 | Invisibilité | Améliorer la fiche ; ne pas acheter de trafic |
| Conversion | Place de marché | Essai intégré | Continu | — | — | A | — | 0 | Utilisateurs gratuits seulement | Revoir la tarification à l'événement |
| Paiement | Apify puis PayPal ou virement | Facturation mensuelle | Le 11 du mois | Relevé | Versement, rapatriement | A ; D pour l'ouverture du compte de versement | Rapprochement | 20 % + calcul | Versement Maroc refusé | Arrêt du produit si aucune voie légale |
| Livraison | Plateforme | Exécutions | À la demande | Source publique | Extraction | A | Taux d'échec des exécutions | Calcul déduit | Site cible modifié | Alerte, correctif par le Constructeur |
| Support | Support (Haiku 5.5 + Sonnet 5.5) | Tickets Apify | Ticket | Journal d'exécution | Réponse, correctif | B | Délai de réponse | Centimes | Avis négatif | Escalade |
| Rétention | — | — | — | — | Fiabilité dans la durée | A | Disponibilité | — | — | — |
| Optimisation | Stratège | Statistiques d'usage | Mensuel | Exécutions, revenus | Retrait des actors sans usage | B | Règle : retrait après 90 jours sous 5 USD/mois [H] | — | — | — |
| Reporting | Tableau de bord | Relevés | Mensuel | Brut, net | Rapport | A | Rapprochement | — | — | — |

**Part automatisable, temps humain et criticité.** 95 % et plus des tâches récurrentes en volume [E] ; 85–95 % selon les chercheurs [H]. Temps résiduel : **0,5 à 1 heure par semaine** [H]. Criticité élevée sur deux points seulement : le choix des sources (conditions d'utilisation, politique d'Anthropic interdisant de contourner les règles d'autres plateformes [F] ([Anthropic AUP](https://www.anthropic.com/legal/aup))) et l'ouverture du compte de versement.

**Difficultés, risques, leviers, validation.** La difficulté est d'être visible parmi 25 787 actors. Le risque principal est un revenu nul ; le risque juridique est le choix d'une cible dont les conditions interdisent la collecte. Le levier est la niche linguistique et géographique. La validation est gratuite : compter les concurrents et leur usage avant d'écrire le premier collecteur, puis confirmer par écrit que le versement vers le Maroc est possible.

---

### E.4 Alertes TED santé / medtech (#65) — score révisé 54

| Rubrique | Contenu |
|---|---|
| Concept exact | Alerte quotidienne et digest hebdomadaire des avis de marchés publics européens dans la santé, la pharmacie et les dispositifs médicaux, filtrés par code CPV et par profil, résumés en français et en anglais |
| Client cible | PME européennes de la santé et exportateurs du Maghreb visant les marchés publics de l'UE |
| Problème résolu | Bruit des alertes généralistes |
| Proposition de valeur | Profondeur verticale ; socle juridique vérifié |
| Preuve de marché disponible | TED est réutilisable commercialement avec attribution, en paquets XML et par API [F] ([TED](https://ted.europa.eu/en/help/data-reuse)). Prix des concurrents : Marchés Online dès 25 EUR/mois [F] ([Marchés Online](https://www.marchesonline.com/abonnement-entreprise)), Stotles dès 75 GBP/mois et Tenders Direct dès 1 359 GBP/an [S] ([Jorpex](https://jorpex.com/compare/best-tender-alert-services/)) |
| Concurrents | Marchés Online, Stotles (avec offre gratuite), Tenders Direct, Tracker, Jorpex, Mercell |
| Prix envisagés et justification | 45 USD/mois [H], dans la fourchette 25–150 EUR des chercheurs. **Ce prix place le produit dans la bande de rétention à 23 %** : c'est sa faiblesse structurelle |
| Tunnel de vente | Identique à E.1 ; rôle recommandé : palier d'entrée et échantillon gratuit du radar, pas produit autonome |

**Scénarios financiers (prix 45 USD ; frais du marchand officiel 2,75 USD ; IA marginale 1 USD ; provision remboursements 1,35 USD ; marge unitaire 39,90 USD ; coûts fixes 100 USD hors structure).**

| Scénario | Échéance | Clients nets [H] | Chiffre d'affaires | Coûts variables | Coûts fixes | Résultat d'exploitation |
|---|---|---|---|---|---|---|
| Prudent | 3 mois | 0 | 0 | 0 | 100 | −100 |
| Prudent | 6 mois | 2 | 90 | 10 | 100 | −20 |
| Prudent | 12 mois | 4 | 180 | 20 | 100 | +60 |
| Central | 3 mois | 3 | 135 | 15 | 100 | +20 |
| Central | 6 mois | 8 | 360 | 41 | 100 | +219 |
| Central | 12 mois | 20 | 900 | 102 | 100 | +698 |
| Favorable (non prévisionnel) | 3 mois | 10 | 450 | 51 | 100 | +299 |
| Favorable (non prévisionnel) | 6 mois | 30 | 1 350 | 153 | 100 | +1 097 |
| Favorable (non prévisionnel) | 12 mois | 80 | 3 600 | 408 | 100 | +3 092 |

| Indicateur [E] | Prudent | Central | Favorable |
|---|---|---|---|
| Résultat cumulé sur 12 mois, hors structure | −282 USD | +3 388 USD | +16 556 USD |
| Idem avec SARL AU | −2 286 USD | +1 384 USD | +14 552 USD |
| ROI à 12 mois sur 300 USD [H], hors structure | −194 % | +1 030 % | +5 418 % |
| Besoin de trésorerie maximal | ~747 USD | ~380 USD | ~300 USD |
| Seuil de rentabilité | 3 clients hors structure (100 ÷ 39,90 = 2,5) ; 7 clients avec SARL AU (267 ÷ 39,90 = 6,7) | | |
| Délai jusqu'au premier revenu [H] | 4 à 8 semaines : c'est le produit le plus rapide à construire, la source étant ouverte | | |

Avec une rétention brute de 23 %, conserver 20 clients nets au douzième mois suppose d'en avoir recruté bien davantage : le scénario central est plus exigeant en acquisition qu'il n'y paraît, et c'est la raison de la décote.

**Coûts d'exploitation.** API IA ~20 USD/mois (préfiltre par code CPV avant tout appel au modèle) [E] ; hébergement ~40 USD ; acquisition ~30 USD [H] ; divers ~10 USD ; marchand officiel 5 % + 0,50 USD, soit 6,1 % à ce prix ; remboursements 3 % [H].

**Système agentique requis.**

| Étape | Agent responsable | Outils | Déclencheur | Données | Actions | Niveau | Contrôles qualité | Coût | Risque de défaillance | Procédure de reprise |
|---|---|---|---|---|---|---|---|---|---|---|
| Veille de marché | Stratège | Recherche web | Mensuel | Prix concurrents | Note | C | Citations | ~1,5 USD | — | Arbitrage |
| Création du produit | Constructeur (Claude Code) | API et paquets XML TED, tests | Ticket approuvé | Schéma eForms | Connecteur, filtres CPV | C | Tests, comparaison des comptages avec TED | Plafond par exécution | Changement de format | Correctif |
| Publication | Collecteur (code) → Classifieur (Haiku 5.5) → Rédacteur (Sonnet 5.5, lots) | Cron | Chaque jour ouvré | Avis TED | Filtre, résumé, attribution de la source | **A** | Schéma, rapprochement des volumes, mention de la source | ~20 USD/mois | Panne de l'API | Reprise sur le paquet quotidien |
| Acquisition | Prospection | Comme E.1 | Lot approuvé | Sociétés santé | Échantillon personnalisé | C | Liste d'exclusion, règles par pays | ~30 USD/mois | Plainte | Suspension |
| Conversion | Page d'offre | Essai | Entrant | — | — | B | — | — | — | — |
| Paiement | Marchand officiel | Checkout | Achat | — | Encaissement | A ; D pour les comptes | Rapprochement | 5 % + 0,50 USD | Gel | Seconde voie |
| Livraison | Chaîne de publication | E-mail | Quotidien | Profil | Alerte | A | Délivrabilité | Inclus | Doublon | Idempotence |
| Support | Support | Boîte partagée | Entrant | Compte | Réponses | B ; C pour l'argent | Plafonds codés | ~0,02 USD par e-mail | Complaisance | Escalade |
| Rétention | Reporting client | Base | Mensuel | Avis pertinents | Récapitulatif, offre de montée vers le radar | B | Recalcul | Centimes | Attrition élevée | Bascule vers l'offre annuelle |
| Optimisation | Stratège | Métriques | Mensuel | Attrition | Propositions | C | Seuils section G | — | — | — |
| Reporting | Tableau de bord | Exports | Hebdomadaire | Recettes, coûts | Rapport | A | Rapprochement | — | — | — |

**Part automatisable, temps humain et criticité.** 95 % en volume [E] ; ~90 % selon les chercheurs [H]. Temps résiduel : **1 à 2 heures par semaine** [H], presque entièrement sur l'approbation des lots de prospection et les exceptions de paiement.

**Difficultés, risques, leviers, validation.** Aucune difficulté technique : la difficulté est d'exister face à des offres gratuites. Le risque est une attrition qui annule l'acquisition. Le levier est de ne pas le vendre seul : il sert de démonstrateur public (pages par catégorie), d'échantillon et de premier palier du radar E.1. Validation : c'est le premier prototype à construire, parce qu'il ne dépend d'aucune vérification juridique en suspens.

---

### E.5 Digest des tendances d'inspection GMP (#68) — score révisé 52

| Rubrique | Contenu |
|---|---|
| Concept exact | Digest bimensuel des constats d'inspection et des lettres d'avertissement publiés par la FDA, des déclarations de non-conformité européennes et des avis de l'OMS, regroupés par thème, en français, avec un angle formation pour les équipes qualité |
| Client cible | Responsables assurance qualité d'usines de marchés émergents ; organismes de formation |
| Problème résolu | Suivre les tendances d'inspection sans abonnement à plusieurs milliers de dollars |
| Proposition de valeur | Synthèse thématique en français, à prix d'équipe |
| Preuve de marché disponible | Newsletter FDAnews à 1 895 USD par an [F, page non revérifiée] ([FDAnews](https://www.fdanews.com/subscriptions)) ; Redica sur devis. openFDA est en domaine public ou CC0, usage commercial autorisé, sauf contenus de tiers [F] ([openFDA](https://open.fda.gov/terms/)). **Les conditions d'EudraGMDP et des listes OMS n'ont pas été vérifiées** |
| Concurrents | Redica, FDAnews, Govzilla ; contenus gratuits ; assistants généralistes |
| Prix envisagés et justification | 59 USD/mois ou 590 USD/an [H], bas de la fourchette 50–200 USD inférée par les chercheurs |
| Tunnel de vente | Contenu gratuit et inscription volontaire ; aucun e-mail à froid vers des contacts marocains |
| Conflit d'intérêts | Moyen : exclure toute mention de l'employeur, de ses sites et de ses fournisseurs ; n'utiliser aucun rapport d'audit ou d'inspection connu par le travail |

**Scénarios financiers (prix 59 USD ; frais du marchand officiel 3,45 USD ; IA marginale 0,50 USD ; provision remboursements 1,77 USD ; marge unitaire 53,28 USD ; coûts fixes 90 USD hors structure).**

| Scénario | Échéance | Clients nets [H] | Chiffre d'affaires | Coûts variables | Coûts fixes | Résultat d'exploitation |
|---|---|---|---|---|---|---|
| Prudent | 3 mois | 0 | 0 | 0 | 90 | −90 |
| Prudent | 6 mois | 1 | 59 | 6 | 90 | −37 |
| Prudent | 12 mois | 3 | 177 | 17 | 90 | +70 |
| Central | 3 mois | 2 | 118 | 11 | 90 | +17 |
| Central | 6 mois | 6 | 354 | 34 | 90 | +230 |
| Central | 12 mois | 15 | 885 | 86 | 90 | +709 |
| Favorable (non prévisionnel) | 3 mois | 8 | 472 | 46 | 90 | +336 |
| Favorable (non prévisionnel) | 6 mois | 20 | 1 180 | 114 | 90 | +976 |
| Favorable (non prévisionnel) | 12 mois | 50 | 2 950 | 286 | 90 | +2 574 |

| Indicateur [E] | Prudent | Central | Favorable |
|---|---|---|---|
| Résultat cumulé sur 12 mois, hors structure | −281 USD | +3 475 USD | +14 318 USD |
| Idem avec SARL AU | −2 285 USD | +1 471 USD | +12 314 USD |
| ROI à 12 mois sur 300 USD [H], hors structure | −194 % | +1 058 % | +4 673 % |
| Besoin de trésorerie maximal | ~754 USD | ~373 USD | ~300 USD |
| Seuil de rentabilité | 2 clients hors structure (90 ÷ 53,28 = 1,7) ; 5 clients avec SARL AU (257 ÷ 53,28 = 4,8) | | |
| Délai jusqu'au premier revenu [H] | 8 à 12 semaines | | |

**Coûts d'exploitation.** API IA ~15 USD/mois [E] ; hébergement ~35 USD ; acquisition ~30 USD [H] ; divers ~10 USD ; marchand officiel 5 % + 0,50 USD ; remboursements 3 % [H].

**Système agentique requis.**

| Étape | Agent responsable | Outils | Déclencheur | Données | Actions | Niveau | Contrôles qualité | Coût | Risque de défaillance | Procédure de reprise |
|---|---|---|---|---|---|---|---|---|---|---|
| Veille de marché | Stratège | Recherche web | Trimestriel | Offres voisines | Note | C | Citations | ~1,5 USD | — | Arbitrage |
| Création du produit | Constructeur (Claude Code) | API openFDA, tests | Ticket approuvé | Schéma des constats | Connecteur, taxonomie de thèmes | C | Tests | Plafond par exécution | Taxonomie instable | Révision |
| Publication | Collecteur (code) → Classifieur (Haiku 5.5) → Rédacteur (Sonnet 5.5) | Cron | Bimensuel | Constats publics | Regroupement, synthèse, liens | B | Lien vers chaque constat, **filtre d'exclusion de l'employeur codé en dur**, ton factuel | ~15 USD/mois | Imputation erronée à un site (risque de diffamation) | Rectificatif ; retrait |
| Acquisition | Contenu gratuit | Site | Publication | Inscriptions volontaires | Diffusion | B | Consentement | ~30 USD/mois | Liste trop petite | Requalifier en contenu d'appel |
| Conversion | Page d'abonnement | Marchand officiel | Entrant | — | — | B | — | — | — | — |
| Paiement | Marchand officiel | Checkout | Achat | — | Encaissement | A ; D pour les comptes | Rapprochement | 5 % + 0,50 USD | — | — |
| Livraison | Chaîne de publication | E-mail | Bimensuel | — | Digest | A | Délivrabilité | Inclus | — | Reprise |
| Support | Support | Boîte partagée | Entrant | — | Réponses | B | Pas d'avis de conformité individuel | Centimes | Glissement vers le conseil | Escalade |
| Rétention | Reporting client | Base | Trimestriel | Thèmes couverts | Récapitulatif | B | — | — | — | — |
| Optimisation | Stratège | Métriques | Trimestriel | Ouvertures, attrition | Propositions | C | Seuils section G | — | — | — |
| Reporting | Tableau de bord | Exports | Mensuel | Recettes, coûts | Rapport | A | Rapprochement | — | — | — |

**Part automatisable, temps humain et criticité.** 90 à 95 % en volume [E] ; 85 % selon les chercheurs [H]. Temps résiduel : **1 à 2 heures par semaine** [H], concentré sur la relecture d'un échantillon avant envoi tant que le filtre d'exclusion n'a pas fait ses preuves.

**Difficultés, risques, leviers, validation.** La difficulté n'est pas de produire le digest mais de le rendre meilleur que ce qu'un responsable qualité obtient d'un assistant en dix minutes. Le risque est double : produit substituable, et proximité avec le métier de l'employeur. Le levier est de le transformer en outil d'acquisition gratuit pour les produits E.1 et E.2, ou en module de formation vendu à l'année à des organismes. Validation : le publier gratuitement six semaines et compter les demandes explicites de version payante ; sans demande, il reste un contenu d'appel.

### Ce que les cinq fiches disent ensemble

Les seuils de rentabilité sont très bas (deux à cinq clients) parce que la production ne coûte presque rien : un bulletin hebdomadaire revient à moins d'un dollar de jetons et la surveillance de 5 000 avis par jour à 83–166 USD par mois [E] ([Anthropic, tarifs](https://platform.claude.com/docs/en/about-claude/pricing)). Ce n'est pas une bonne nouvelle en soi : un coût d'entrée négligeable vaut aussi pour les concurrents, et les scénarios prudents montrent qu'un produit sans acquisition perd environ 270 à 630 USD par an hors structure et plus de 2 000 USD par an si une SARL AU est créée trop tôt. La décision de structure, et non le coût de l'IA, est le premier poste qui peut rendre le projet déficitaire.


---

## F. Top 3 investment cases — trois paris complémentaires sur une même chaîne

Les trois cas retenus ne sont pas trois entreprises : ce sont trois débouchés d'un même pipeline de veille, choisis parce qu'ils diffèrent par le canal d'acquisition, par le rail d'encaissement et par le profil de conflit d'intérêts. Si l'un échoue, les deux autres ne tombent pas pour la même raison.

| | Cas 1 — Radar d'appels d'offres santé (E.1, avec TED E.4 comme premier module) | Cas 2 — Veille cosmétiques / compléments (E.2), extensible aux dispositifs médicaux | Cas 3 — Actors Apify (E.3) |
|---|---|---|---|
| Justification économique | Ancres de prix publiques 49–342 USD/mois ; l'oubli d'un avis coûte une vente à l'acheteur ; marge unitaire ~89 USD ; seuil à 2–4 clients | Pas de concurrent tarifé ; actualité réglementaire forte ; seul cas où l'expertise du mandant sert sans exposer l'employeur | Coût marginal quasi nul : les collecteurs existent déjà pour les cas 1 et 2 ; facturation et distribution par la plateforme |
| Canal d'acquisition | Échantillon personnalisé par petits lots hors Maroc + pages publiques par catégorie | Contenu gratuit, inscription volontaire, associations professionnelles | Recherche interne de la place de marché |
| Rail d'encaissement | Marchand officiel puis virement bancaire au Maroc | Marchand officiel pour l'étranger ; virement ou agrégateur local au Maroc | Versement Apify (PayPal ou autre), à confirmer |
| Résultat mensuel au 12e mois, prudent / central / favorable [E] | +126 / +923 / +3 403 USD | +21 / +587 / +2 000 USD | −11 / +157 (illustratif) / +1 530 USD |
| Besoin de trésorerie maximal [E] | ~1 100 USD hors structure | ~1 060 USD hors structure | ~420 USD |
| Niveau de risque | Commercial élevé, financier faible, juridique moyen (conditions des portails, périmètre de l'employeur) | Commercial élevé (demande non prouvée), financier faible, juridique faible à moyen | Commercial élevé (loterie), financier très faible, juridique faible si les sources sont choisies sur conditions lues |
| Temps du mandant en régime établi [H] | 2–3 h/semaine | 2–4 h/semaine | 0,5–1 h/semaine |
| Séquencement | **Premier.** Semaines 1 à 4 sur TED seul ; portails des bailleurs ajoutés après lecture de leurs conditions | **Deuxième**, lancé seulement si le cas 1 a produit au moins un pilote payé ou si sa validation a échoué pour une raison propre à sa niche | **En parallèle, sans priorité** : publication des collecteurs dès qu'ils sont stables |

Additionnés à coûts fixes non mutualisés, les trois cas donnent au douzième mois environ **+136 USD par mois dans le scénario prudent, +1 667 USD dans le scénario central et +6 933 USD dans le scénario favorable**, avant coût de structure et avant impôt de l'exploitant [E]. Le cumul sur douze mois va de −1 244 USD (prudent) à +7 927 USD (central), hors structure. Avec une SARL AU à 20 000 MAD par an, le scénario prudent devient une perte d'environ 3 250 USD sur l'année. Le pari est donc asymétrique mais petit : la perte plausible se compte en quelques milliers de dirhams hors structure, le gain central en un complément de revenu de l'ordre de 15 000 à 17 000 MAD par mois au bout d'un an, et rien dans les sources ne permet d'attribuer une probabilité à l'un ou à l'autre.

Le digest GMP (E.5) n'est pas un quatrième cas d'investissement : il sert de contenu d'appel gratuit. La veille réglementaire pharma Maroc (#61) reste la meilleure opportunité « sur le papier » pour ce profil et la plus dangereuse pour son emploi ; elle ne se rouvre qu'avec une autorisation écrite de l'employeur.

---

## G. Autonomous operating system blueprint — un cron, une base, une file d'approbation

### Principe d'architecture : des pipelines courts et vérifiables, pas un « PDG IA »

Les preuves orientent le choix. Les erreurs des agents se composent : même sur des tâches bien spécifiées, les taux de réussite mesurés par Anthropic sont de 93 % pour Haiku 5.5 sur un lot de 79 tâches et de 92,8 % pour Opus 5.5 sur un sous-ensemble de SWE-bench Pro, soit 5 à 8 % d'échecs par étape qui se cumulent le long d'une chaîne [F] ([Anthropic](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)). Sur Vending-Bench 2, les meilleurs modèles atteignent environ 16 500 USD quand Andon Labs estime une bonne stratégie à 63 000 USD [F] ([Andon Labs](https://andonlabs.com/evals/vending-bench-2)). Et un superviseur de la même famille de modèles partage les angles morts de ses exécutants : ce sont les règles codées en dur, pas un modèle plus intelligent, qui ont rétabli les marges de Project Vend [F] ([Anthropic](https://www.anthropic.com/research/project-vend-2)). L'architecture recommandée est donc la plus simple possible : tâches planifiées, file en base de données, exécutants idempotents, validation déterministe entre chaque étape, et aucune autorité discrétionnaire des agents sur l'argent ou sur les engagements contractuels.

### Routage des modèles : Fable 5.2 seulement là où il paie

| Rôle | Modèle | Justification sourcée |
|---|---|---|
| Classement, extraction, tri du support | Haiku 5.5 (0,10 / 0,50 USD par million de jetons) | ~0,011 USD par tâche courte réussie ; garder chaque requête sous 100 000 jetons, au-delà le prix est multiplié par 5 [F] ([tarifs](https://platform.claude.com/docs/en/about-claude/pricing)) |
| Rédaction des résumés, brouillons de réponses, exécutants outillés | Sonnet 5.5 (2 / 10 USD), en lots quand le délai le permet | 87,6 % de réussite à 0,11 USD par tâche résolue [F] ([optimisation](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)) |
| Orchestration, construction de code, escalade sur échec | Opus 5.5 (4 / 20 USD) | Opus 5.5 orchestrant des sous-agents Sonnet 5.5 coûte environ un tiers de moins qu'Opus seul pour le même score ; l'escalade « effort bas puis reprise des échecs » résout ~97 % à ~0,17 USD par tâche [F] |
| Revue stratégique hebdomadaire, arbitrages difficiles | **Fable 5.2 (8 / 40 USD), effort bas ou moyen, quelques appels par semaine** | Comme orchestrateur, Fable 5.2 coûte 19 % de plus pour le même score ; en recherche approfondie, 4,3 fois le coût de Sonnet 5.5 « sans gain mesurable » ; un conseiller Fable 5.1 apporte 1,7 point pour 2,1 fois le coût [F] |

Deux remises structurent la facture. Le traitement par lots retire 50 % et se cumule avec le cache ; sans cache, une boucle d'agent coûte 3 à 7 fois plus cher [F]. Mais le cache par défaut ne vit que cinq minutes : pour des charges à faible trafic, la remise fiable est le traitement par lots [H chercheurs]. Le routage vers un second fournisseur ne se justifie plus par le prix (Haiku 5.5 est au niveau du palier le moins cher d'OpenAI [F] ([OpenAI](https://developers.openai.com/api/docs/pricing))) mais par la résilience et par la vérification indépendante.

### Évaluation des briques

| Brique | Verdict | Fait décisif |
|---|---|---|
| API Claude sous conditions commerciales, un espace de travail par activité | **Socle** | Plafonds de dépense par organisation et par espace de travail ; palier de départ plafonné à 500 USD/mois, 1 000 USD au palier suivant [F] ([limites](https://platform.claude.com/docs/en/api/rate-limits)) |
| Abonnement personnel (Max 100 USD, Ultra 200 USD) | Poste de l'opérateur humain, pas moteur de production | Les conditions grand public interdisent l'accès automatisé hors des voies permises par Anthropic ; l'abonnement inclut 100 ou 200 USD de crédits API mensuels [F] ([conditions](https://www.anthropic.com/legal/consumer-terms), [crédits](https://platform.claude.com/docs/en/about-claude/api-credits-for-subscribers)) |
| Claude Code sans interface (`claude -p`) | **Retenu** pour la construction et la maintenance | Budget maximal par exécution, sortie JSON, refus de tout ce qui demanderait une approbation [F] ([doc](https://code.claude.com/docs/en/headless)) |
| Agent SDK | Retenu si un exécutant outillé doit tourner sur son propre serveur | Même boucle d'agent que Claude Code, hébergée par l'exploitant [F] |
| Managed Agents | Option, pas dépendance | Bêta ; 0,08 USD par heure de session active en plus des jetons ; pas de remise par lots ; non éligible à la rétention zéro des données [F] ([doc](https://platform.claude.com/docs/en/managed-agents/overview)) |
| Tâches planifiées cloud de Claude Code | Automatisations personnelles du mandant seulement | Aperçu de recherche, intervalle minimal d'une heure, rattachées à un compte individuel [F] ([doc](https://code.claude.com/docs/en/routines)) |
| Équipes d'agents | Écarté | Expérimental ; environ 7 fois les jetons d'une session standard [F] ([coûts](https://code.claude.com/docs/en/costs)) |
| MCP | Utile pour exposer les données aux agents clients ; pas nécessaire en interne | Statut du connecteur non vérifié en direct par les chercheurs [I] |
| n8n | Acceptable en auto-hébergement pour un usage interne ; **interdit de le revendre ou de l'intégrer à un produit payant sans accord commercial** | Licence « Sustainable Use » : usage « pour vos propres besoins internes » [F] ([licence](https://raw.githubusercontent.com/n8n-io/n8n/master/LICENSE.md)) ; n8n Cloud 20–50 EUR/mois [F] ([n8n](https://n8n.io/pricing/)) |
| LangGraph / LangSmith | Non nécessaire à cette échelle | LangSmith gratuit jusqu'à 5 000 traces/mois, 39 USD par siège au-delà [F] ([LangChain](https://www.langchain.com/pricing)) |
| Temporal, Inngest, Trigger.dev | À adopter seulement si des flux doivent attendre des heures une approbation ou reprendre un état multi-étapes | Trigger.dev 10 USD/mois, Inngest gratuit jusqu'à 50 000 exécutions [F] ([Trigger.dev](https://trigger.dev/pricing), [Inngest](https://www.inngest.com/pricing)) |
| Zapier / Make | Colle à faible volume uniquement | 5 000 avis par jour consommeraient ~150 000 tâches par mois, bien au-delà du palier à 169 USD [E] ([Zapier](https://zapier.com/pricing)) |
| **Cron + file Postgres + exécutants idempotents** | **Choix par défaut** | Suffisant tant que les tâches durent quelques minutes et qu'il y a moins d'une douzaine de types de flux [H chercheurs] |

### Composants, statut et coût

| Composant | Réalisation | Statut |
|---|---|---|
| Base persistante (sources, avis, clients, envois, coûts, décisions) | Postgres auto-hébergé ou Supabase Pro à 25 USD/mois [F] ([Supabase](https://supabase.com/pricing)) | (1) Disponible ; schéma (2) à développer |
| Tâches planifiées | Cron sur un VPS (DigitalOcean 6–48 USD/mois [F] ([DigitalOcean](https://www.digitalocean.com/pricing/droplets))) ou Cloudflare Workers à 5 USD/mois [F] ([Cloudflare](https://developers.cloudflare.com/workers/platform/pricing/)) | (1) Disponible |
| Mémoire | Tables de la base (profils clients, décisions du mandant, liste d'exclusion) ; fichiers de consignes versionnés | (2) À développer ; les magasins de mémoire des Managed Agents sont en bêta non vérifiée en direct (3) |
| Observabilité, journaux, alertes | Langfuse auto-hébergé ou offre gratuite (50 000 unités/mois) [F] ([Langfuse](https://langfuse.com/pricing)) ; alertes par e-mail | (1) Disponible ; règles d'alerte (2) à développer |
| Tests automatisés et vérification indépendante | Validation de schéma, rapprochement de totaux, liens vivants, jeu d'or par source ; second passage par un autre modèle sur échantillon | (2) À développer ; vérification par un second fournisseur (3) envisagée |
| E-mail transactionnel | Resend gratuit jusqu'à 3 000 e-mails/mois, 20 USD ensuite [F] ([Resend](https://resend.com/pricing)) | (1) Disponible |
| Tableau de bord financier central | Page unique alimentée par les exports du marchand officiel et le coût par exécution renvoyé par l'API | (2) À développer |
| File d'approbation du mandant | Table « en attente » + notification ; rien ne part sans validation pour les actions de niveau C | (2) À développer |
| Agent d'acquisition autonome, lancement automatique de nouvelles activités, négociation de partenariats par agent | — | (3) Envisagé seulement ; aucune preuve publique qu'un agent acquière des clients B2B de façon rentable |

### Garde-fous

| Risque | Garde-fou | Déclencheur de suspension |
|---|---|---|
| Dérive des coûts | Plafond mensuel par espace de travail ; budget en dollars par exécution, jamais par `max_tokens` (les tours tronqués sont facturés) [F] | Coût IA du jour supérieur à trois fois la moyenne mobile [H] : arrêt des planificateurs |
| Anomalie de production | Rapprochement des volumes avec la source, alerte « zéro avis » ou « dix fois le volume » | Suspension des envois, pas de la collecte |
| Fraude et litiges | Aucun outil d'argent chez les agents ; plafond de remboursement codé en dur ; balayage des soldes du marchand officiel | Premier litige de paiement : gel du compte client et alerte |
| Plainte ou désinscription contestée | Lien de désinscription, liste de suppression, preuve de consentement | Une plainte : arrêt de toute prospection jusqu'à décision du mandant |
| Non-conformité | Liste d'exclusion de l'employeur, liste de pays à consentement, registre des conditions lues par source | Toute source sans conditions lues est refusée par défaut |
| Injection d'instructions | L'agent qui lit du contenu non fiable (e-mails, pages web) n'a ni outil d'envoi d'argent, ni suppression, ni secret ; les secrets restent hors du contexte du modèle | Comportement hors gabarit détecté par validation de sortie : mise en quarantaine du message |
| Interrupteur général | Script unique qui désactive les planificateurs et révoque les clés API | Activable par le mandant ; la réactivation exige son accord |

Le risque d'injection n'est pas théorique : pour Claude Opus 5, la presse rapporte d'après les fiches système d'Anthropic un taux de réussite d'attaque indirecte de 0,2 % en une tentative et 2,0 % en quinze [S] ([Xenospectrum](https://xenospectrum.com/en/claude-opus-5-prompt-injection/)) ; aucun chiffre n'a été trouvé pour Fable 5.2, Opus 5.5, Sonnet 5.5 ou Haiku 5.5. Sur une boîte qui reçoit des milliers de messages, il faut supposer un succès occasionnel et en limiter le rayon. La politique d'usage d'Anthropic rend par ailleurs le déployeur responsable de tout ce que l'agent fait par ses outils, interdit de faire passer un agent pour un humain et exige que tout agent en contact avec des tiers se déclare comme IA [F, lu via résumé] ([Anthropic AUP](https://www.anthropic.com/legal/aup)).

### Estimation de coût mensuel du système

| Scénario | Charge type | Jetons API | Supervision Fable 5.2 | Infrastructure et outils (recherche web, calcul, base, orchestrateur, e-mail, observabilité, navigateur, abonnement opérateur optionnel) | Total arrondi par les chercheurs [E] |
|---|---|---|---|---|---|
| Léger | 1 bulletin hebdomadaire, ~300 e-mails, ~500 documents, quelques agents planifiés | 20–80 USD | 5–20 USD | ~7–165 USD | **70–200 USD** |
| Moyen | Bulletins quotidiens, ~3 000 e-mails outillés, veille d'appels d'offres, ~10 000 documents | 300–800 USD | 40–120 USD | ~210–580 USD | **500–1 200 USD** |
| Lourd | ~20 000 e-mails, 50 000 documents et plus, ~2 000 sessions d'agent, automatisation de navigateur | 2 500–6 500 USD | 200–600 USD | ~730–2 200 USD | **3 000–8 000 USD** |

Ces totaux sont des calculs des chercheurs sur des volumes de jetons supposés, hors temps humain, frais du marchand officiel, impôts et données payantes ([Anthropic, tarifs](https://platform.claude.com/docs/en/about-claude/pricing)). Le portefeuille recommandé relève du scénario léger. Le scénario moyen ne tient sous le plafond de 1 000 USD du second palier d'API qu'en bas de fourchette ; le scénario lourd exige un relèvement de palier demandé à l'avance. Le premier facteur de variation est l'architecture, pas le volume : passer de boucles d'agent ouvertes à des pipelines fixes change la ligne « jetons » d'un facteur 3 à 10.

### Modèle d'allocation du capital et de réinvestissement

Les seuils ci-dessous sont des **règles proposées par le rédacteur** ; seuls les repères d'attrition, de cache et de conversion proviennent de sources.

| Décision | Seuil objectif proposé | Repère sourcé |
|---|---|---|
| Lancer une nouvelle activité | L'activité précédente a obtenu au moins 3 pilotes payés, ou a été arrêtée proprement ; temps du mandant ≤ 3 h/semaine sur quatre semaines ; file d'approbation vidée chaque semaine | — |
| Augmenter le budget marketing | Coût d'acquisition mesuré sur au moins 10 clients, remboursé en ≤ 6 mois de marge ; attrition mensuelle ≤ 3,5 % | Cible d'attrition mensuelle sous 3,5 % pour un revenu par compte inférieur à 100 USD, sous 2,5 % au-dessus [S] ([ChartMogul](https://chartmogul.com/lp/saas-churn)) |
| Améliorer le produit | Attrition mensuelle > 5 % deux mois de suite, ou plus d'un avis manqué signalé par mois, ou plus de 0,5 ticket par client et par mois | — |
| Réduire le coût de l'IA | Coût IA > 10 % du chiffre d'affaires, ou part d'entrées lues en cache < 80 %, ou Fable 5.2 > 15 % de la dépense en jetons | Une boucle saine lit une médiane de 84 % de ses entrées en cache ; sous ~80 %, quelque chose casse le cache [F] ([Anthropic](https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence)) |
| Augmenter les prix | Essai → payant ≥ 25 % et attrition ≤ 2,5 % sur trois mois : +20 % pour les nouveaux clients uniquement | Essai sans carte → payant ~18 % à la médiane, 25 % au quartile supérieur [S] ([Userpilot](https://userpilot.com/blog/free-trial-conversion-rate/)) |
| Entrer sur un nouveau marché | ≥ 20 % des demandes entrantes viennent d'une zone ou d'une langue non couverte, et les conditions des sources de cette zone sont lues | — |
| Arrêter une activité déficitaire | Après le sixième mois : résultat d'exploitation négatif trois mois de suite **et** moins de 3 clients payants ; ou blocage juridique ; ou temps du mandant > 5 h/semaine pendant quatre semaines | Repère de planification : 0–200 USD de MRR à six mois pour un produit lancé [H chercheurs] |
| Réallouer | Le budget va à l'activité dont la marge sur coûts variables par heure du mandant est la plus élevée sur le trimestre | — |

**Décisions qui exigent toujours l'accord préalable du mandant** : signature de tout contrat et acceptation de toutes conditions d'utilisation ; création de structure, ouverture de compte, KYC, déclarations fiscales et de change ; toute dépense au-dessus du plafond mensuel approuvé ; tout changement de prix ; tout remboursement au-dessus du plafond codé et toute réponse à un litige, une réclamation ou une mise en demeure ; chaque lot de premier contact commercial ; l'ajout d'une source de données dont les conditions n'ont pas été lues ; toute publication sous une nouvelle marque ; tout ce qui touche au périmètre de l'employeur ; la réactivation après un arrêt d'urgence.


---

## H. Financial comparison — trois budgets, et les contraintes marocaines qui les bornent

Hypothèse de conversion rappelée : 1 USD ≈ 10 MAD, 1 EUR ≈ 11 MAD. C'est une hypothèse de travail à actualiser, pas un cours constaté.

Trois règles marocaines bornent chaque budget avant même la question du marché. Un particulier, donc un auto-entrepreneur non inscrit au registre du commerce, ne dispose pour payer par carte des fournisseurs étrangers (API, hébergement, outils) que de la **dotation e-commerce de 20 000 MAD par an**, soit environ 167 USD par mois ; une société nouvellement créée obtient 50 000 MAD dès le premier jour, puis jusqu'à 200 000 MAD selon l'impôt payé [F] ([IGOC 2026](http://www.oc.gov.ma/sites/default/files/2026-01/IGOC%202026_1.pdf)). Les recettes d'export de services doivent être rapatriées intégralement sous 90 jours, et jusqu'à 70 % peuvent être conservées en devises pour régler des dépenses professionnelles à l'étranger [F]. Enfin, le statut d'auto-entrepreneur de services plafonne les encaissements à 200 000 MAD par an et les taxe à 1 % libératoire [F loi ; S presse pour les taux] ([Loi 114-13](https://adala.justice.gov.ma/api/uploads/2024/05/07/Loi%20Relative%20au%20statut%20de%20l%E2%80%99auto-entrepreneur-1715071318209.pdf), [Le Matin](https://lematin.ma/economie/auto-entrepreneur-ce-que-prevoit-le-regime-fiscal-en-2026/361537)).

| | Microcapital : 0–3 000 MAD (~0–300 USD) | Intermédiaire : 3 000–15 000 MAD (~300–1 500 USD) | Développement : 15 000–60 000 MAD (~1 500–6 000 USD) |
|---|---|---|---|
| Activités accessibles | Validation du cas 1 sur TED (prototype, digest concierge) ; lecture des conditions des sources ; premiers actors Apify (capital estimé < 200 USD [H]) ; à titre de loterie, téléchargements Etsy (< 100 USD [H]) | Cas 1 en production pendant 6 à 12 mois sur l'architecture légère ; cas 3 ; démarrage du cas 2 ; statut d'auto-entrepreneur si sa compatibilité est confirmée ; marchand officiel | Les trois cas sur infrastructure commune pendant 12 mois ; création d'une SARL AU si nécessaire ; consultations juridique et comptable ; petits tests payants de quelques centaines de dollars pour mesurer l'intention, jamais pour inférer un coût d'acquisition |
| Coûts [E sauf mention] | 2 à 3 mois d'architecture légère au plancher (~70 USD/mois) ; inscription auto-entrepreneur gratuite, timbre ~50 MAD [S] ([ClicPaie](https://clicpaie.ma/blogs/auto-entrepreneur-maroc/)) | 840 à 1 500 USD pour douze mois à 70–125 USD/mois ; ~400 USD de mise en place [H] | Création SARL AU 1 500–2 300 MAD en direct ou 3 660–6 110 MAD par prestataire ; fonctionnement annuel 15 000–50 000 MAD [S] ([ClicPaie](https://clicpaie.ma/blogs/creer-sarl-maroc/)) ; infrastructure 840–2 400 USD/an |
| Ce qui reste hors de portée | Toute structure sociétaire ; toute acquisition payante | Architecture « moyenne » ; SARL AU sans consommer le budget | Architecture « moyenne » (500–1 200 USD/mois, soit 60 000–144 000 MAD/an) ; rachat d'un SaaS rentable : la médiane demandée est ~190 000 USD et 6 000 USD n'achètent qu'environ 165 USD de revenu mensuel [S] ([BigIdeasDB](https://bigideasdb.com/state-of-saas-valuations-2026)) |
| Contrainte marocaine qui mord | La dotation de 20 000 MAD n'est pas atteinte ; **le premier encaissement exige un véhicule de facturation**, et l'acceptation d'un auto-entrepreneur par le KYC des marchands officiels n'est pas vérifiée [I] | La dotation de 20 000 MAD/an couvre l'architecture légère jusqu'à ~165 USD/mois, pas au-delà ; le compte en devises pour particuliers à revenus de source étrangère lève ce plafond à hauteur de 70 % des recettes rapatriées, pratique bancaire à confirmer [I] ; plafond de 200 000 MAD d'encaissements | La société ouvre 50 000 MAD de dotation carte, le régime d'importation de services par virement et le compte exportateur à 70 % ; en contrepartie IS à 20 %, cotisation minimale de 0,25 % (plancher 3 000 MAD, exonérée 36 mois), retenue sur dividendes de 11,25 % en 2026 à confirmer [S] ([Upsilon](https://upsilon-consulting.com/calcul-impot-societes-bareme-progressif/), [Upsilon](https://upsilon-consulting.com/taux-de-retenue-a-la-source-sur-dividendes/)) |
| Risques | Revenu nul (cas le plus probable d'après les distributions observées) ; temps du mandant | Perte de 300 à 1 250 USD dans le scénario prudent ; règle des 30 % de retenue au-delà de 80 000 MAD facturés à un même client, dont l'application à un payeur unique non résident comme un marchand officiel n'est pas vérifiée [I] | La structure seule peut absorber de 25 % à plus de 100 % du budget ; coût fixe dû même sans chiffre d'affaires |
| Verdict | **Point de départ recommandé** : tout ce qui précède la preuve de demande tient dans ce budget | Budget cible une fois trois pilotes payés obtenus | À n'engager que sur déclencheur : plafond d'auto-entrepreneur en vue, refus bancaire du compte en devises, dépenses étrangères > 20 000 MAD/an, ou incompatibilité confirmée du statut avec le salariat |

L'arbitrage auto-entrepreneur contre SARL AU se lit dans le calcul illustratif des chercheurs : pour 50 000 MAD de recettes annuelles, l'auto-entrepreneur conserve environ 49 500 MAD avant cotisations sociales, la SARL AU environ 21 300 MAD après 20 000 MAD de frais de structure, IS et retenue sur dividendes ; pour 200 000 MAD, 198 000 contre 127 800 MAD [E chercheurs]. La société ne se justifie donc pas par la fiscalité à cette échelle ; elle se justifie par l'accès aux devises et par la sécurité juridique si le cumul avec le salariat est refusé à l'auto-entrepreneur. Deux écarts ne sont pas des options : ouvrir un compte ou constituer une société à l'étranger sans autorisation de l'Office des Changes, et conserver des soldes sur une plateforme de paiement au-delà des délais de rapatriement.

---

## I. Validation roadmap — sept, trente et quatre-vingt-dix jours, en argent et non en inscriptions

**La Phase 1 est une recherche : rien n'a été lancé.** Tout ce qui, dans cette feuille de route, implique de contacter un prospect ou un fournisseur, de dépenser, d'ouvrir un compte ou de publier, **exige l'autorisation explicite du mandant et relève de la Phase 2**. Les seuils chiffrés sont des propositions du rédacteur, à fixer avant le premier envoi : les inscriptions surestiment la demande de deux à trois ordres de grandeur (400 inscrits Product Hunt pour un client payant dans un cas documenté [S] ([Indie Hackers](https://www.indiehackers.com/post/400-signups-from-product-hunt-1-paying-customer-what-4-days-taught-me-about-launch-vs-traction-7c0aacf745))).

| Horizon | Actions du mandant (décisions et autorisations) | Travaux des agents (sans contact extérieur tant que non autorisé) | Indicateurs de demande réelle | Critères de passage [H] | Conditions d'abandon [H] |
|---|---|---|---|---|---|
| J+7 | Relire le contrat de travail et la politique d'activités extérieures ; décider de la demande d'autorisation écrite ; saisir un avocat en droit du travail, un expert-comptable et le guichet commerce extérieur de la banque avec la liste de questions de l'annexe ; arrêter la liste d'exclusion (produits, fournisseurs, clients, appels d'offres de l'employeur) | Lire et consigner les conditions d'utilisation de chaque portail visé ; prototype sur TED ; jeu d'or de 50 avis vérifiés à la main ; décompte des concurrents et de leur usage sur Apify ; rédaction des questions écrites aux marchands officiels (envoi après autorisation) | Aucun à ce stade | Aucun blocage juridique ; au moins une voie d'encaissement confirmée par écrit ; rappel du prototype ≥ 95 % sur le jeu d'or ; au moins deux portails de bailleurs aux conditions compatibles | Clause d'exclusivité sans dérogation de l'employeur : arrêt ; aucune voie d'encaissement légale : arrêt ; conditions des portails incompatibles : repli sur TED seul et sur le cas 2 |
| J+30 | Approuver la liste nominative de 10 à 20 prospects et chaque lot ; approuver l'offre de pilote payant et son prix | Digest concierge gratuit pendant deux à trois semaines pour les prospects approuvés, puis lien de paiement pour un pilote annuel à prix réduit ; trois numéros gratuits du bulletin du cas 2 ; publication du premier actor | **Paiements reçus** ; demandes écrites de devis ; réponses demandant une couverture précise. Les ouvertures, clics et inscriptions ne comptent pas | Au moins 3 pilotes payés pour 20 prospects qualifiés au plus, ou au moins 300 USD prépayés | Aucun paiement après 30 prospects qualifiés et deux formulations de l'offre : arrêt de la niche et report de l'effort sur le cas 2 ; une plainte : arrêt de la prospection |
| J+90 | Choisir le statut juridique sur avis de l'expert-comptable ; valider les prix définitifs ; décider du lancement payant du cas 2 | Mise en production du cas 1 ; ajout des portails validés ; tableau de bord ; file d'approbation ; garde-fous de la section G | Clients payants actifs ; renouvellements ; attrition du premier trimestre ; temps réel du mandant | Au moins 5 clients payants ou 400 USD de MRR ; temps du mandant ≤ 3 h/semaine ; coût IA ≤ 10 % du chiffre d'affaires ; aucun incident de conformité | Moins de 3 clients payants : arrêt de l'offre par abonnement, les collecteurs ne subsistant que comme actors Apify ; temps du mandant > 5 h/semaine quatre semaines de suite ; toute objection de l'employeur |

Le digest concierge contredit temporairement la contrainte « pas d'opérations » : c'est un coût de validation borné, réalisable par e-mail et sans appel, et c'est aussi le test direct de l'hypothèse la plus fragile, à savoir que l'offre se vend sans conversation.

---

## J. Final investment decision — sept réponses

**1. Meilleur rapport profit potentiel / risque / investissement.** Le radar d'appels d'offres santé des bailleurs, démarré sur TED. Il combine le meilleur score révisé (60/100), un besoin de trésorerie maximal d'environ 1 100 USD hors structure, un seuil de rentabilité de deux à quatre clients et un résultat central de l'ordre de 920 USD par mois au douzième mois [E]. Le risque dominant est commercial, pas financier : dans le scénario prudent, il rapporte 126 USD par mois après un an.

**2. Opportunité la plus automatisable.** Les actors Apify : plus de 95 % des tâches récurrentes, 0,5 à 1 heure par semaine, aucune prospection. Parmi les abonnements, les alertes TED sont les seules dont l'étape de publication atteint le niveau A. Dans les deux cas, l'automatisation élevée va de pair avec le revenu attendu le plus faible.

**3. Premières recettes les plus rapides.** Un pilote payé du radar, obtenu par digest concierge : six à dix semaines après l'autorisation de la Phase 2 [H]. C'est le seul chemin où l'encaissement est déclenché par une demande explicite adressée à des prospects nommés. Un actor Apify peut encaisser en quatre à huit semaines, mais peut aussi ne jamais rien encaisser.

**4. Meilleur potentiel de croissance à douze mois.** Le radar, par extension de zones, historique d'attributions et palier équipe ; puis, comme prolongement, l'intelligence réglementaire panafricaine (#62), dont les sources fragmentées forment une barrière mais dont l'automatisation n'est que de 60 à 70 %. Aucun des cinq produits n'a un potentiel « élevé » selon les preuves disponibles.

**5. Activité qui minimise le temps du mandant.** Apify seul, à moins d'une heure par semaine, pour un revenu attendu proche de zéro. Le compromis réaliste est le radar plus Apify, autour de trois à quatre heures par semaine en régime établi [H]. Aucune activité ne descend à zéro : contrats, KYC, approbations de prospection, remboursements et litiges restent humains.

**6. Portefeuille recommandé sur infrastructure partagée.** Radar d'appels d'offres santé (avec TED comme palier d'entrée), veille cosmétiques/compléments, actors Apify, le digest GMP servant de contenu gratuit. Les trois partagent collecteurs, base, file d'approbation et tableau de bord. Menés de front, ils demanderaient 4,5 à 8 heures par semaine [H] : le séquencement de la section F n'est pas une prudence, c'est la condition pour rester sous le plafond de temps du mandant.

**7. Informations essentielles encore manquantes.** Sept éléments décident de tout et ne peuvent venir que du mandant ou de tiers : le texte du contrat de travail et de la politique d'activités extérieures de l'employeur, ainsi que le périmètre exact de ses produits, marchés et appels d'offres ; l'avis d'un avocat sur le cumul salariat et activité indépendante, que les chercheurs n'ont pu fonder sur aucun article ni aucune jurisprudence marocaine ; l'avis d'un expert-comptable sur l'éligibilité au statut d'auto-entrepreneur, sur la règle des 30 % face à un payeur unique non résident et sur les taux 2026 non lus dans le texte officiel ; la confirmation écrite d'un marchand officiel qu'il accepte un vendeur marocain sous le statut retenu, la situation de Lemon Squeezy après son rachat par Stripe n'étant pas éclaircie ; la pratique de la banque pour le compte en devises et le rapatriement ; les conditions de réutilisation de chaque portail d'appels d'offres ; et la seule donnée qui manque à toute la littérature consultée : **un client qui paie**. Aucune étude ne la remplace, et le budget microcapital de la section H (moins de 3 000 MAD) suffit à aller la chercher [E].

La conclusion à retenir tient en une inversion. L'idée de départ était de déployer du capital et des agents pour bâtir des entreprises autonomes ; les preuves montrent que le capital n'est pas la contrainte, que l'autonomie complète n'existe pas encore, et que l'avantage du mandant, son expertise pharmaceutique, est aussi sa principale exposition. Ce qui reste est plus étroit et plus honnête : un pipeline de veille sur données publiques, quelques clients à une centaine de dollars par mois, une file d'approbation hebdomadaire, et une décision d'investir qui se prend après le premier paiement reçu, pas avant.

---

## Annexe 1 — Contraintes marocaines : ce qui est établi et ce qui reste à valider

### Statuts juridiques

| Sujet | Ce que disent les sources | Niveau de preuve | À valider auprès de |
|---|---|---|---|
| Auto-entrepreneur : définition et plafonds | Personne physique exerçant à titre individuel ; plafond de 200 000 MAD d'encaissements pour les services, 500 000 MAD pour le commerce ; dispense de comptabilité et de registre du commerce ; domiciliation au domicile possible ; **aucune exclusion des salariés dans la loi** ([Loi 114-13](https://adala.justice.gov.ma/api/uploads/2024/05/07/Loi%20Relative%20au%20statut%20de%20l%E2%80%99auto-entrepreneur-1715071318209.pdf)) | [F] | — |
| Auto-entrepreneur : fiscalité | 1 % libératoire sur les encaissements de services ; hors champ de la TVA ; retenue de 30 % au-delà de 80 000 MAD par an facturés à un même client ; dépassement du plafond deux années consécutives = sortie du statut ([Le Matin](https://lematin.ma/economie/auto-entrepreneur-ce-que-prevoit-le-regime-fiscal-en-2026/361537)) | [S presse relayant le guide de la DGI] | Expert-comptable : application des 30 % à un client non résident ; classement des abonnements numériques (services ou commerce) |
| Cumul auto-entrepreneur et salariat | Un guide l'admet si l'activité diffère de l'emploi, sans clause d'exclusivité ni concurrence ([ClicPaie](https://clicpaie.ma/blogs/auto-entrepreneur-maroc/)) ; un autre affirme l'incompatibilité sans citer d'article ([Humantal](https://humantal.ma/ressources/statut-auto-entrepreneur-maroc-guide-complet)) | [S, sources en conflit] | Avocat ; Barid Al-Maghrib ou Maroc PME |
| Cotisations sociales de l'auto-entrepreneur | Barème trimestriel de 300 à 3 600 MAD reproduit par un guide, libellés douteux | [I] | CNSS ; expert-comptable |
| SARL / SARL AU | Pas de capital minimal légal ; création 1 500–6 110 MAD ; fonctionnement annuel 15 000–50 000 MAD ; délai 7–30 jours ([ClicPaie](https://clicpaie.ma/blogs/creer-sarl-maroc/), [Upsilon](https://upsilon-consulting.com/cout-creation-sarl-maroc-2026/)) | [S, cabinets] | Expert-comptable |
| Impôts de la société | IS 20 % sous 100 MMAD de bénéfice ; cotisation minimale 0,25 %, plancher 3 000 MAD, exonération 36 mois ; retenue sur dividendes 11,25 % en 2026 (source incohérente en interne), 10 % en 2027 ; charge combinée ~29 % du bénéfice distribué ([Upsilon](https://upsilon-consulting.com/calcul-impot-societes-bareme-progressif/), [ClicPaie](https://clicpaie.ma/blogs/impot-societes-maroc/), [Upsilon](https://upsilon-consulting.com/taux-de-retenue-a-la-source-sur-dividendes/)) | [S, non lu dans le CGI 2026] | Expert-comptable, sur le CGI 2026 et la circulaire 737 |
| Transformation | Transformer l'activité en société entraîne la radiation du registre des auto-entrepreneurs | [F] | — |

### TVA et marchand officiel

L'export de services est exonéré avec droit à déduction si le client est établi hors du Maroc, le contrat libellé en devises et le service utilisé à l'étranger (art. 92-I-1° du CGI) [S, cabinet] ([Upsilon](https://upsilon-consulting.com/tva-export-services-maroc/)). Un marchand officiel est juridiquement le vendeur auprès du client final et collecte la TVA européenne et les taxes de vente américaines ; l'entreprise marocaine lui fait une vente B2B à l'export [H chercheurs, connaissance de fond non revérifiée]. Depuis le 11 juin 2026, les prestataires étrangers de services numériques doivent collecter la TVA marocaine auprès des consommateurs marocains (art. 115 bis) [S presse] ([Hespress](https://fr.hespress.com/473798-tva-la-dgi-deploie-son-dispositif-visant-les-services-digitaux-etrangers.html)). À valider par l'expert-comptable : seuil d'assujettissement, traitement d'une activité mixte Maroc et export, traitement des paiements reçus d'un marchand officiel.

### Paiements réellement accessibles

| Voie | Statut pour un résident marocain | Niveau de preuve |
|---|---|---|
| Stripe | Non disponible : Maroc absent des 51 marchés ([Stripe](https://stripe.com/global)) | [F] |
| Lemon Squeezy | Maroc dans la liste des pays à virement bancaire ; versements deux fois par mois après 13 jours de rétention ([Lemon Squeezy](https://docs.lemonsqueezy.com/help/getting-started/supported-countries)) ; maintien des inscriptions après le rachat par Stripe non éclairci | [F] + [I] |
| Paddle | Maroc absent de la liste des pays vendeurs non pris en charge ; vérification officielle par l'API /countries ; un développeur marocain dit l'utiliser ([Paddle](https://www.paddle.com/help/start/account-verification/which-countries-are-supported-by-paddle), [Reddit](https://reddit.sentinel-team.org/posts/1r75dun/snapshots/2026-02-21T00%3A02%3A01.038049Z)) | [F] + anecdote |
| Polar | Ne verse pas au Maroc ([Polar](https://polar.sh/docs/merchant-of-record/supported-countries)) ; une note de recherche disait l'inverse d'après un résumé, la page primaire prévaut | [F] |
| Freemius | Maroc listé d'après un résumé ([Freemius](https://freemius.com/help/documentation/selling-with-freemius/supported-countries)) | [S] |
| PayPal | Réception et retrait possibles ; retrait en MAD via CashPlus depuis septembre 2025 ; fonds à retirer sous 30 jours ; coût total estimé 3–4 % et plus ([Médias24](https://medias24.com/2025/09/16/cashplus-lance-via-son-application-le-retrait-des-soldes-paypal-en-mad/), [Grey](https://grey.co/blog/wise-vs-paypal-vs-payoneer-which-works-better-for-moroccans)) | [S] |
| Payoneer | Comptes de réception en devises, retrait vers une banque marocaine avec ~2–3 % de conversion ([Grey](https://grey.co/blog/wise-vs-paypal-vs-payoneer-which-works-better-for-moroccans)) | [S, blog concurrent] |
| Wise | Disponibilité pour les résidents contestée entre sources | [I] |
| Etsy Payments ; programme partenaire YouTube | Disponibles ([Etsy](https://help.etsy.com/hc/articles/115015710408), [YouTube](https://support.google.com/youtube/answer/7101720)) | [F] |
| Google Play marchand ; Shopify Payments | Indisponibles ([Google Play](https://support.google.com/googleplay/android-developer/answer/9306917), [Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/supported-countries)) | [F] |
| Encaissement domestique | CMI et acquéreurs, agrégateurs Payzone, YouCan Pay ; commissions estimées 1,2–2,5 % ; interchange plafonné à 0,5 % en juillet 2026 ([TelQuel](https://telquel.ma/instant-t/2026/07/10/paiement-electronique-bank-al-maghrib-baisse-les-frais-dinterchange-a-05_1998527/)) | [S] |
| Virement SWIFT sur facture | Voie admise par l'instruction des changes | [F] |
| Crypto-actifs | Projet de loi encore à l'examen en avril 2026 ; exclu | [S] |

À valider : confirmation écrite de chaque prestataire pour le statut retenu ; versement vers le Maroc pour Apify, Shopify, Atlassian et Apple, non confirmé. Les gels de fonds de 90 à 180 jours rapportés par des marchands (sources intéressées) [S] ([terms.law](https://terms.law/FAQ/payment-processors/stripe-holds-faq.html)) justifient de garder une seconde voie approuvée.

### Réglementation des changes (IGOC 2026, en vigueur le 1er janvier 2026)

Tous les points suivants sont lus dans le texte officiel ([IGOC 2026](http://www.oc.gov.ma/sites/default/files/2026-01/IGOC%202026_1.pdf)) ; la numérotation des articles est à revérifier dans le PDF. Rapatriement intégral des recettes d'export de services sous 90 jours. Comptes en devises ou en dirhams convertibles pour les exportateurs inscrits au registre du commerce, crédités à 70 % des recettes rapatriées. Comptes équivalents pour les personnes physiques non inscrites disposant de revenus de source étrangère, sur déclaration écrite à la banque. Dotation e-commerce de 20 000 MAD par personne physique, 50 000 MAD pour une société nouvelle, jusqu'à 200 000 MAD selon l'impôt payé, 2 000 000 MAD pour une jeune entreprise innovante labellisée. Importation de services par virement réservée aux personnes inscrites au registre du commerce. **Ouverture de compte et constitution d'avoirs à l'étranger soumises à autorisation** ; dernière régularisation spontanée close le 31 décembre 2024. Le terme « auto-entrepreneur » n'apparaît pas dans le texte : la lecture selon laquelle il relève du régime des personnes physiques est une inférence des chercheurs. À valider auprès de la banque : ouverture effective du compte en devises pour un auto-entrepreneur payé par un marchand officiel, pièces demandées, traitement des paiements d'outils étrangers par carte ou par virement.

### Protection des données et prospection

La loi 09-08 reste en vigueur : notification préalable des traitements à la CNDP, encadrement des transferts hors du Maroc, y compris vers des API de modèles hébergées à l'étranger [S, cabinet] ([Upsilon](https://upsilon-consulting.com/cndp-loi-09-08-protection-donnees-personnelles-maroc/)). La prospection par e-mail ou SMS exige le consentement préalable, sauf client existant pour des produits analogues, sans exception B2B, sous peine de 3 mois à 1 an d'emprisonnement et de 20 000 à 200 000 MAD d'amende [F] ([CNDP](https://www.cndp.ma/wp-content/uploads/2025/07/fiche_CNDP_Prospection_RT_fr.pdf)). Servir des clients européens ajoute le RGPD ; le Maroc ne bénéficie pas d'une décision d'adéquation [H chercheurs, connaissance de fond]. La réponse de conception est de ne traiter que des données publiques et de ne détenir aucune donnée client au-delà du compte. À valider par un avocat : formalité CNDP pour le fichier clients et prospects ; règles de prospection B2B par pays cible ; lois 31-08, 53-05 et 43-20, non étudiées.

### Emploi et conflit d'intérêts

| Point | Source | Niveau de preuve |
|---|---|---|
| Devoir de loyauté pendant le contrat ; une clause d'exclusivité interdit toute autre activité ; l'employeur peut autoriser par écrit | ([La Vie Éco](https://www.lavieeco.com/?p=56484)) | [S presse] |
| La clause de non-concurrence relève de la pratique et de la jurisprudence, pas du Code du travail | ([ReKrute](https://www.rekrute.com/emplois-clause-de-non-concurrence-un-vide-juridique-a-combler-conseils-carriere-759.html)) | [S] |
| La divulgation de secrets professionnels est citée parmi les fautes graves (art. 39, loi 65-99) | ([CMS](https://cms.law/en/mar/legal-updates/ce-qu-il-faut-savoir-sur-le-licenciement-pour-faute-grave-au-maroc)) | [S, cabinet] |
| Pharmaciens, médecins et autres professions exclus du statut d'auto-entrepreneur | ([Le Matin](https://lematin.ma/economie/auto-entrepreneur-ce-que-prevoit-le-regime-fiscal-en-2026/361537)) | [S] |
| Publicité et vente de médicaments réservées et encadrées par la loi 17-04 ; vente en ligne interdite | ([Hespress](https://fr.hespress.com/404325-achat-en-ligne-de-medicaments-les-mises-en-gardes-du-ministre-tahraoui.html)) | [S presse] |

Règles de conduite retenues dans ce rapport, à faire valider par un avocat marocain : n'utiliser que des sources publiques avec un journal de source par donnée ; exclure produits, fournisseurs, appels d'offres et clients de l'employeur ; ne jamais travailler sur le temps ni le matériel de l'employeur ; ne jamais facturer son propre employeur ; rester en deçà des actes réglementés (pharmacien responsable, personne qualifiée en pharmacovigilance, avis médical ou juridique) ; privilégier le produit de données traçables au produit d'opinion, parce qu'un client ne distingue pas un « avis d'expert » d'une information d'initié. Les chercheurs n'ont trouvé ni article du Code du travail ni jurisprudence marocaine sur le cumul d'activités, ni règle sectorielle sur le statut d'une société d'information en santé : ces trois points sont ouverts.

---

## Annexe 2 — Note méthodologique

Sept flux de recherche parallèles ont été conduits le 11 novembre 2026 avec recherche web : services B2B productisés ; micro-SaaS, API et produits de données ; contenu, affiliation et e-commerce ; intelligence pharma, réglementaire et appels d'offres ; conformité, fiscalité et paiements au Maroc ; architecture d'agents et coûts ; acquisition et contre-expertise. Le présent rapport synthétise leurs sept notes sans recherche additionnelle.

**Ce qui a été vérifié sur page primaire** : les tarifs et limites de l'API Claude ; les prix publics d'une vingtaine d'éditeurs ; les listes de pays de Stripe, Google Play, Shopify Payments, Etsy, Lemon Squeezy, Paddle et Polar ; le texte de l'IGOC 2026 et de la loi 114-13 ; la fiche de la CNDP ; les règles de contenu de Google, YouTube, KDP, Etsy et Medium ; les rapports de ChartMogul, Seer Interactive, beehiiv, Flippa et Smartlead ; les comptes rendus d'Anthropic sur Project Vend et sur l'optimisation des coûts.

**Ce qui ne l'a pas été** : la majorité des prix de concurrents de second rang, issus d'agrégateurs ou de résumés de recherche ; les chiffres TrustMRR, affichés par les fondateurs et non audités ; les textes du CGI 2026, de la loi 09-08, de la loi 17-04 et du Code du travail, connus par des cabinets et par la presse ; les conditions d'utilisation des portails d'appels d'offres marocain, onusien et des bailleurs ; les fiches système d'Anthropic sur l'injection d'instructions ; les règles européennes et américaines mentionnées comme connaissance de fond. La politique d'usage d'Anthropic a été lue par l'intermédiaire d'un outil de résumé, dans une version datée du 12 novembre 2026.

**Ce qui est estimé et non mesuré** : toutes les parts d'automatisation, tous les capitaux de départ, toutes les difficultés, toutes les dispositions à payer dans la pharmacie, tous les volumes de jetons, tous les nombres de clients des scénarios et tous les scores de la section D.

**Ce qui n'existe pas dans les sources** : un revenu vérifié d'opérateur solo absent dans la quasi-totalité des catégories ; un jeu de données indépendant sur la survie des agences IA ou des micro-SaaS ; une mesure de la conversion d'un e-mail à froid en achat sans appel ; une donnée sur des vendeurs marocains vendant à l'Europe ou aux États-Unis ; une étude de la demande marocaine ou africaine pour ces produits. La plupart des repères d'acquisition proviennent de fournisseurs qui vendent le canal mesuré.

**Aucun client n'a été contacté, aucun test de demande n'a été exécuté, aucune dépense n'a été engagée, aucun compte n'a été ouvert.** Ce rapport n'est ni un avis juridique, ni un avis fiscal.


---

## Annexe 3 — Sources citées (URL et dates)

Toutes les pages ont été consultées par les chercheurs le **11 novembre 2026**, sauf mention contraire dans le texte ; la date de publication est indiquée dans le corps du rapport quand elle est connue. La liste reprend chaque URL citée dans ce rapport, classée par domaine ; le libellé est celui de la première citation. Les niveaux de preuve ([F], [S], [AD]) figurent à l'endroit de la citation. Nombre de sources distinctes : **175**.

| Domaine | Libellé de citation | URL | Consultation |
|---|---|---|---|
| 9to5google.com | 9to5Google | <https://9to5google.com/2020/03/12/chrome-web-store-fee/> | 11/11/2026 |
| adala.justice.gov.ma | Loi 114-13 | <https://adala.justice.gov.ma/api/uploads/2024/05/07/Loi%20Relative%20au%20statut%20de%20l%E2%80%99auto-entrepreneur-1715071318209.pdf> | 11/11/2026 |
| air.io | AIR | <https://air.io/en/air-data-findings/youtube-monetization-statistics-2026> | 11/11/2026 |
| aisdr.com | AiSDR | <https://aisdr.com/pricing/> | 11/11/2026 |
| andonlabs.com | Andon Labs | <https://andonlabs.com/evals/vending-bench-2> | 11/11/2026 |
| anthropic.com | Anthropic AUP | <https://www.anthropic.com/legal/aup> | 11/11/2026 |
| anthropic.com | conditions | <https://www.anthropic.com/legal/consumer-terms> | 11/11/2026 |
| anthropic.com | Anthropic, Project Vend 2 | <https://www.anthropic.com/research/project-vend-2> | 11/11/2026 |
| apify.com | Apify | <https://apify.com/datapilot/public-tender-procurement-alerts/api/mcp> | 11/11/2026 |
| apify.com | Apify | <https://apify.com/tagadanar/french-public-tenders> | 11/11/2026 |
| apify.com | Apify | <https://apify.com/taroyamada/procurement-intel-actor/api/mcp> | 11/11/2026 |
| apple.com | Apple | <https://www.apple.com/in/newsroom/2020/11/apple-announces-app-store-small-business-program/> | 11/11/2026 |
| arblogz.pages.dev | arblogz | <https://arblogz.pages.dev/blog/clarivate-lsh-division-sale-cortellis-cri> | 11/11/2026 |
| atlassian.com | Atlassian | <https://www.atlassian.com/blog/developer/updates-to-marketplace-revenue-share-2026> | 11/11/2026 |
| authorsguild.org | Authors Guild | <https://authorsguild.org/news/amazon-adds-to-kdp-generative-ai-policy-caps-daily-self-publishing-uploads/> | 11/11/2026 |
| autorfp.ai | AutoRFP | <https://autorfp.ai/blog/loopio-pricing> | 11/11/2026 |
| barchart.com | Barchart | <https://www.barchart.com/story/news/730560/adbe-q1-deep-dive-ai-transition-ceo-succession-and-freemium-push-shape-outlook> | 11/11/2026 |
| barn2.com | Barn2 | <https://barn2.com/blog/shopify-app-store-saturation/> | 11/11/2026 |
| beehiiv.com | beehiiv | <https://www.beehiiv.com/blog/the-state-of-newsletters-2026> | 11/11/2026 |
| beehiiv.com | beehiiv | <https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026> | 11/11/2026 |
| bigideasdb.com | BigIdeasDB | <https://bigideasdb.com/how-to-sell-a-wordpress-plugin> | 11/11/2026 |
| bigideasdb.com | BigIdeasDB | <https://bigideasdb.com/shopify-app-vs-wordpress-plugin> | 11/11/2026 |
| bigideasdb.com | BigIdeasDB | <https://bigideasdb.com/state-of-indie-saas-revenue-2026> | 11/11/2026 |
| bigideasdb.com | BigIdeasDB | <https://bigideasdb.com/state-of-saas-valuations-2026> | 11/11/2026 |
| blog.mean.ceo | mean.ceo | <https://blog.mean.ceo/?p=11219> | 11/11/2026 |
| blog.tiime.fr | Tiime | <https://blog.tiime.fr/comparatif-plateformes-agreees-de-facturation-%C3%A9lectronique-en-2026> | 11/11/2026 |
| blogdumoderateur.com | Blog du Modérateur | <https://www.blogdumoderateur.com/ia-cyber-budgets-10-chiffres-numerique-tpe-pme-2026/> | 11/11/2026 |
| capeb.fr | CAPEB | <https://www.capeb.fr/actualites/service-veille-marches-publics> | 11/11/2026 |
| capterra.co.uk | Capterra UK | <https://www.capterra.co.uk/software/1063362/rightresponse-ai> | 11/11/2026 |
| capterra.com | Capterra | <https://www.capterra.com/p/10049639/Pharmatext/> | 11/11/2026 |
| capterra.com | Capterra | <https://www.capterra.com/p/160189/Dext/pricing/> | 11/11/2026 |
| chartmogul.com | ChartMogul | <https://chartmogul.com/lp/saas-churn> | 11/11/2026 |
| chartmogul.com | ChartMogul, déc. 2025 | <https://chartmogul.com/reports/saas-retention-the-ai-churn-wave/> | 11/11/2026 |
| chatbase.co | Chatbase | <https://www.chatbase.co/pricing> | 11/11/2026 |
| clay.com | Clay | <https://www.clay.com/pricing> | 11/11/2026 |
| clicpaie.ma | ClicPaie | <https://clicpaie.ma/blogs/auto-entrepreneur-maroc/> | 11/11/2026 |
| clicpaie.ma | ClicPaie | <https://clicpaie.ma/blogs/creer-sarl-maroc/> | 11/11/2026 |
| clicpaie.ma | ClicPaie | <https://clicpaie.ma/blogs/impot-societes-maroc/> | 11/11/2026 |
| cms.law | CMS | <https://cms.law/en/mar/legal-updates/ce-qu-il-faut-savoir-sur-le-licenciement-pour-faute-grave-au-maroc> | 11/11/2026 |
| cndp.ma | CNDP | <https://www.cndp.ma/wp-content/uploads/2025/07/fiche_CNDP_Prospection_RT_fr.pdf> | 11/11/2026 |
| code.claude.com | coûts | <https://code.claude.com/docs/en/costs> | 11/11/2026 |
| code.claude.com | doc | <https://code.claude.com/docs/en/headless> | 11/11/2026 |
| code.claude.com | doc | <https://code.claude.com/docs/en/routines> | 11/11/2026 |
| connect.wolfia.com | Wolfia | <https://connect.wolfia.com/blog/conveyor-reviews-pricing-alternatives> | 11/11/2026 |
| dev.to | DEV Community | <https://dev.to/_350df62777eb55e1/real-numbers-freemium-chrome-extension-monetization-after-6-months-5hga> | 11/11/2026 |
| dev.to | DEV Community | <https://dev.to/sessionzero_ai/2000-runs-in-3-days-real-revenue-data-from-launching-13-korean-scrapers-on-apify-211h> | 11/11/2026 |
| developers.cloudflare.com | Cloudflare | <https://developers.cloudflare.com/workers/platform/pricing/> | 11/11/2026 |
| developers.google.com | Google Search Central | <https://developers.google.com/search/docs/essentials/spam-policies> | 11/11/2026 |
| developers.openai.com | OpenAI | <https://developers.openai.com/api/docs/pricing> | 11/11/2026 |
| digiday.com | Digiday | <https://digiday.com/media/politicos-new-fda-focused-subscription-product-costs-75k-year/> | 11/11/2026 |
| digitalocean.com | DigitalOcean | <https://www.digitalocean.com/pricing/droplets> | 11/11/2026 |
| docparser.com | Docparser | <https://www.docparser.com/pricing/> | 11/11/2026 |
| docs.apify.com | Apify | <https://docs.apify.com/actors/monetize.md> | 11/11/2026 |
| docs.apify.com | Apify | <https://docs.apify.com/actors/publishing/monetize/monthly-payouts.md> | 11/11/2026 |
| docs.lemonsqueezy.com | Lemon Squeezy | <https://docs.lemonsqueezy.com/help/getting-started/supported-countries> | 11/11/2026 |
| docs.rapidapi.com | RapidAPI | <https://docs.rapidapi.com/docs/payouts-and-finance> | 11/11/2026 |
| drugpatentwatch.com | DrugPatentWatch | <https://www.drugpatentwatch.com/pricing/> | 11/11/2026 |
| etsy.com | Etsy | <https://www.etsy.com/legal/creativity> | 11/11/2026 |
| evaluate.com | Evaluate | <https://www.evaluate.com/pricing/> | 11/11/2026 |
| fdanews.com | FDAnews | <https://www.fdanews.com/subscriptions> | 11/11/2026 |
| first-mrr.com | first-mrr | <https://first-mrr.com/study/seobot> | 11/11/2026 |
| fr.hespress.com | Hespress | <https://fr.hespress.com/404325-achat-en-ligne-de-medicaments-les-mises-en-gardes-du-ministre-tahraoui.html> | 11/11/2026 |
| fr.hespress.com | Hespress | <https://fr.hespress.com/470286-cryptomonnaie-le-gouvernement-accelere-la-regulation-pour-contrer-le-blanchiment-et-encadrer-le-marche.html> | 11/11/2026 |
| fr.hespress.com | Hespress | <https://fr.hespress.com/473798-tva-la-dgi-deploie-son-dispositif-visant-les-services-digitaux-etrangers.html> | 11/11/2026 |
| freemius.com | Freemius | <https://freemius.com/help/documentation/selling-with-freemius/supported-countries> | 11/11/2026 |
| getapp.com | GetApp | <https://www.getapp.com/all-software/a/bibliovigilance/> | 11/11/2026 |
| getapp.com | GetApp | <https://www.getapp.com/operations-management-software/a/freyrsubmitpro/> | 11/11/2026 |
| getlasso.co | Lasso | <https://getlasso.co/amazon-affiliate-commission-rate/> | 11/11/2026 |
| getlatka.com | Latka | <https://getlatka.com/companies/freemius.com/interviews/freemius-vova-feldman-2025> | 11/11/2026 |
| globalsolo.global | GlobalSolo | <https://www.globalsolo.global/blog/stripe-vs-paddle-vs-lemon-squeezy-2026> | 11/11/2026 |
| go.pharmazie.com | pharmazie.com | <https://go.pharmazie.com/pricing> | 11/11/2026 |
| grey.co | Grey | <https://grey.co/blog/wise-vs-paypal-vs-payoneer-which-works-better-for-moroccans> | 11/11/2026 |
| help.apify.com | Apify | <https://help.apify.com/en/articles/8684010-how-does-actor-monetization-work> | 11/11/2026 |
| help.etsy.com | Etsy | <https://help.etsy.com/hc/articles/115015710408> | 11/11/2026 |
| help.medium.com | Medium | <https://help.medium.com/hc/en-us/articles/22576852947223> | 11/11/2026 |
| help.shopify.com | Shopify | <https://help.shopify.com/en/manual/payments/shopify-payments/supported-countries> | 11/11/2026 |
| heyrosie.com | Rosie | <https://www.heyrosie.com/pricing> | 11/11/2026 |
| humantal.ma | Humantal | <https://humantal.ma/ressources/statut-auto-entrepreneur-maroc-guide-complet> | 11/11/2026 |
| ifc.org | IFC | <https://www.ifc.org/en/stories/2025/answering-africas-call-for-private-investment-in-pharma-manufacturing> | 11/11/2026 |
| indiehackers.com | Indie Hackers | <https://www.indiehackers.com/post/400-signups-from-product-hunt-1-paying-customer-what-4-days-taught-me-about-launch-vs-traction-7c0aacf745> | 11/11/2026 |
| indiehackers.com | Indie Hackers | <https://www.indiehackers.com/post/how-i-turned-my-copycats-into-customers-from-open-source-directory-to-5k-month-boilerplate-ce615af4f6> | 11/11/2026 |
| indiehackers.com | Indie Hackers | <https://www.indiehackers.com/post/i-built-a-simple-directory-of-job-boards-4-years-ago-it-just-passed-100k-60da9ba8f2> | 11/11/2026 |
| inngest.com | Inngest | <https://www.inngest.com/pricing> | 11/11/2026 |
| instantly.ai | Instantly | <https://instantly.ai/pricing> | 11/11/2026 |
| intercom.com | Intercom | <https://www.intercom.com/pricing> | 11/11/2026 |
| jobbers.io | Jobbers | <https://www.jobbers.io/medical-writing-freelancing-pharma-healthcare-regulatory-content-2026/> | 11/11/2026 |
| jorpex.com | Jorpex | <https://jorpex.com/compare/best-tender-alert-services/> | 11/11/2026 |
| jorpex.com | Jorpex | <https://jorpex.com/compare/tender-monitoring-tools/> | 11/11/2026 |
| jorpex.com | Jorpex | <https://jorpex.com/fr/compare/explore-alternative/> | 11/11/2026 |
| kdp.amazon.com | KDP | <https://kdp.amazon.com/en_US/help/topic/G200672390> | 11/11/2026 |
| kolabtree.com | Kolabtree | <https://www.kolabtree.com/find-an-expert/subject/regulatory-affairs> | 11/11/2026 |
| kolonell.com | Kolonell | <https://kolonell.com/fr/blog/plateforme-gestion-appels-offres-btp-casablanca-cout-2026> | 11/11/2026 |
| l2b.co.za | L2B | <https://www.l2b.co.za/Tenders/Tender-Pricing> | 11/11/2026 |
| lafabriquedunet.fr | La Fabrique du Net | <https://www.lafabriquedunet.fr/logiciels/tech/standard-telephonique/standard-telephonique-ia> | 11/11/2026 |
| langchain.com | LangChain | <https://www.langchain.com/pricing> | 11/11/2026 |
| langfuse.com | Langfuse | <https://langfuse.com/pricing> | 11/11/2026 |
| lavieeco.com | La Vie Éco | <https://www.lavieeco.com/?p=56484> | 11/11/2026 |
| lavieeco.com | La Vie Éco | <https://www.lavieeco.com/argent/le-paiement-digital-un-catalyseur-de-croissance-pour-les-tpme/> | 11/11/2026 |
| ledesk.ma | Le Desk | <https://ledesk.ma/datadesk/distribution-du-medicament-les-limites-chiffrees-du-modele-selon-le-conseil-de-la-concurrence/> | 11/11/2026 |
| lematin.ma | Le Matin | <https://lematin.ma/economie/auto-entrepreneur-ce-que-prevoit-le-regime-fiscal-en-2026/361537> | 11/11/2026 |
| lemonsqueezy.com | Lemon Squeezy | <https://www.lemonsqueezy.com/pricing> | 11/11/2026 |
| letsdatascience.com | Let's Data Science | <https://letsdatascience.com/news/googles-ai-search-features-cut-publisher-traffic-data-from-s-d1c19012> | 11/11/2026 |
| linkedin.com | LinkedIn | <https://www.linkedin.com/help/linkedin/answer/a1341387> | 11/11/2026 |
| marchesonline.com | Marchés Online | <https://www.marchesonline.com/abonnement-entreprise> | 11/11/2026 |
| meddeviceguide.com | MedDeviceGuide | <https://meddeviceguide.com/blog/medical-device-regulatory-consulting-hourly-rates-region-guide> | 11/11/2026 |
| medias24.com | Médias24 | <https://medias24.com/2025/06/10/autorisations-pharmaceutiques-lammps-reprend-les-attributions-du-sgg-des-le-16-juin/> | 11/11/2026 |
| medias24.com | Médias24 | <https://medias24.com/2025/09/16/cashplus-lance-via-son-application-le-retrait-des-soldes-paypal-en-mad/> | 11/11/2026 |
| medias24.com | Médias24 | <https://medias24.com/2026/04/15/enquete-complements-alimentaires-dans-les-coulisses-dun-marche-bien-insuffisamment-regule-1659623/> | 11/11/2026 |
| medias24.com | Médias24 | <https://medias24.com/2026/07/28/pharmacovigilance-amm-surveillance-du-marche-ce-qui-va-changer-1731843/> | 11/11/2026 |
| n8n.io | n8n | <https://n8n.io/pricing/> | 11/11/2026 |
| natlawreview.com | NatLawReview | <https://natlawreview.com/press-releases/apify-bets-1m-independent-developers-building-ais-missing-tools> | 11/11/2026 |
| newsletter.microns.io | Microns | <https://newsletter.microns.io/p/2025-year-in-review> | 11/11/2026 |
| oc.gov.ma | IGOC 2026, Office des Changes | <http://www.oc.gov.ma/sites/default/files/2026-01/IGOC%202026_1.pdf> | 11/11/2026 |
| open.fda.gov | openFDA | <https://open.fda.gov/terms/> | 11/11/2026 |
| opencorporates.com | OpenCorporates | <https://opencorporates.com/pricing/> | 11/11/2026 |
| openopps.com | OpenOpps | <https://www.openopps.com/pricing> | 11/11/2026 |
| openwebninja.com | OpenWeb Ninja | <https://www.openwebninja.com/blog/best-job-data-apis-2026> | 11/11/2026 |
| outrank.so | Outrank | <https://www.outrank.so/pricing> | 11/11/2026 |
| paddle.com | Paddle | <https://www.paddle.com/help/start/account-verification/which-countries-are-supported-by-paddle> | 11/11/2026 |
| paddle.com | Paddle | <https://www.paddle.com/pricing> | 11/11/2026 |
| peec.ai | Peec | <https://peec.ai/pricing> | 11/11/2026 |
| pharmacompass.com | PharmaCompass | <https://www.pharmacompass.com/manufacturers-suppliers-distributors-services-fdf> | 11/11/2026 |
| platform.claude.com | crédits | <https://platform.claude.com/docs/en/about-claude/api-credits-for-subscribers> | 11/11/2026 |
| platform.claude.com | Anthropic, optimisation des coûts | <https://platform.claude.com/docs/en/about-claude/models/optimizing-for-cost-and-intelligence> | 11/11/2026 |
| platform.claude.com | Anthropic, tarifs | <https://platform.claude.com/docs/en/about-claude/pricing> | 11/11/2026 |
| platform.claude.com | limites | <https://platform.claude.com/docs/en/api/rate-limits> | 11/11/2026 |
| platform.claude.com | doc | <https://platform.claude.com/docs/en/managed-agents/overview> | 11/11/2026 |
| podnews.net | Podnews | <https://podnews.net/update/ai-slop-overtakes-humans> | 11/11/2026 |
| polar.sh | Polar | <https://polar.sh/docs/merchant-of-record/supported-countries> | 11/11/2026 |
| pressgazette.co.uk | Press Gazette | <https://pressgazette.co.uk/newsletters/newsletters-2026-prices-retention-churn/> | 11/11/2026 |
| printful.com | Printful | <https://www.printful.com/blog/print-on-demand-statistics> | 11/11/2026 |
| prisync.com | Prisync | <https://prisync.com/pricing/> | 11/11/2026 |
| rai-3d8.pages.dev | RAi | <https://rai-3d8.pages.dev/> | 11/11/2026 |
| raw.githubusercontent.com | licence | <https://raw.githubusercontent.com/n8n-io/n8n/master/LICENSE.md> | 11/11/2026 |
| reddit.sentinel-team.org | Reddit | <https://reddit.sentinel-team.org/posts/1r75dun/snapshots/2026-02-21T00%3A02%3A01.038049Z> | 11/11/2026 |
| rekrute.com | ReKrute | <https://www.rekrute.com/emplois-clause-de-non-concurrence-un-vide-juridique-a-combler-conseils-carriere-759.html> | 11/11/2026 |
| resend.com | Resend | <https://resend.com/pricing> | 11/11/2026 |
| ruzuku.com | Ruzuku | <https://www.ruzuku.com/learn/articles/course-pricing-benchmarks> | 11/11/2026 |
| seerinteractive.com | Seer Interactive | <https://seerinteractive.com/insights/aio-impact-on-google-ctr-2026-update> | 11/11/2026 |
| shopify.dev | Shopify.dev | <https://shopify.dev/docs/apps/launch/distribution/revenue-share> | 11/11/2026 |
| signalcensus.pages.dev | SignalCensus | <https://signalcensus.pages.dev/articles/apify-store-may-2026-25787-actors-480k-mau> | 11/11/2026 |
| smartlead.ai | Smartlead | <https://www.smartlead.ai/benchmarks> | 11/11/2026 |
| stripe.com | Stripe | <https://stripe.com/global> | 11/11/2026 |
| supabase.com | Supabase | <https://supabase.com/pricing> | 11/11/2026 |
| support.google.com | Google Play Console | <https://support.google.com/googleplay/android-developer/answer/9306917> | 11/11/2026 |
| support.google.com | YouTube | <https://support.google.com/youtube/answer/1311392> | 11/11/2026 |
| support.google.com | YouTube | <https://support.google.com/youtube/answer/7101720> | 11/11/2026 |
| synthflow.ai | Synthflow | <https://synthflow.ai/pricing> | 11/11/2026 |
| teach.udemy.com | Udemy | <https://teach.udemy.com/enabling-investment-subscription-terms-update/> | 11/11/2026 |
| techcrunch.com | TechCrunch | <https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have> | 11/11/2026 |
| techcrunch.com | TechCrunch | <https://techcrunch.com/2026/03/10/ai-powered-apps-struggle-with-long-term-retention-new-report-shows> | 11/11/2026 |
| ted.europa.eu | TED | <https://ted.europa.eu/en/help/data-reuse> | 11/11/2026 |
| telquel.ma | TelQuel | <https://telquel.ma/instant-t/2026/05/21/marches-publics-nadia-fettah-annonce-54-000-entreprises-inscrites-et-une-hausse-de-408-des-bons-de-commande_1990710/> | 11/11/2026 |
| telquel.ma | TelQuel | <https://telquel.ma/instant-t/2026/06/11/le-secteur-des-complements-alimentaires-soppose-au-monopole-des-pharmacies_1993544/> | 11/11/2026 |
| telquel.ma | TelQuel | <https://telquel.ma/instant-t/2026/07/10/paiement-electronique-bank-al-maghrib-baisse-les-frais-dinterchange-a-05_1998527/> | 11/11/2026 |
| terms.law | terms.law | <https://terms.law/FAQ/payment-processors/stripe-holds-faq.html> | 11/11/2026 |
| toolradar.com | Toolradar | <https://toolradar.com/tools/volza/pricing> | 11/11/2026 |
| trigger.dev | Trigger.dev | <https://trigger.dev/pricing> | 11/11/2026 |
| triplewhale.com | Triple Whale | <https://triplewhale.com/blog/facebook-ads-benchmarks> | 11/11/2026 |
| trustmrr.com | TrustMRR | <https://trustmrr.com/> | 11/11/2026 |
| trustmrr.com | TrustMRR | <https://trustmrr.com/startup/findajobboard> | 11/11/2026 |
| trustmrr.com | TrustMRR | <https://trustmrr.com/startup/qatestingjobs-com> | 11/11/2026 |
| upsilon-consulting.com | Upsilon | <https://upsilon-consulting.com/calcul-impot-societes-bareme-progressif/> | 11/11/2026 |
| upsilon-consulting.com | Upsilon | <https://upsilon-consulting.com/cndp-loi-09-08-protection-donnees-personnelles-maroc/> | 11/11/2026 |
| upsilon-consulting.com | Upsilon | <https://upsilon-consulting.com/cout-creation-sarl-maroc-2026/> | 11/11/2026 |
| upsilon-consulting.com | Upsilon | <https://upsilon-consulting.com/taux-de-retenue-a-la-source-sur-dividendes/> | 11/11/2026 |
| upsilon-consulting.com | Upsilon | <https://upsilon-consulting.com/tva-export-services-maroc/> | 11/11/2026 |
| upwork.com | Upwork | <https://www.upwork.com/press/releases/upworks-in-demand-skills-2026-demand-for-top-ai-skills-more-than-doubles-as-ai-is-embedded-into-everyday-work> | 11/11/2026 |
| userpilot.com | Userpilot | <https://userpilot.com/blog/free-trial-conversion-rate/> | 11/11/2026 |
| voxbooster.com | VoxBooster | <https://voxbooster.com/blog/digital-course-sales-statistics-2026/> | 11/11/2026 |
| weglot.com | Weglot | <https://www.weglot.com/pricing> | 11/11/2026 |
| woodpecker.co | Woodpecker citant Belkins | <https://woodpecker.co/blog/cold-email-statistics/%20> | 11/11/2026 |
| worldfirst.com | WorldFirst | <https://www.worldfirst.com/af/blog/online-sellers/how-does-etsy-pay-you-africa/> | 11/11/2026 |
| xenospectrum.com | Xenospectrum | <https://xenospectrum.com/en/claude-opus-5-prompt-injection/> | 11/11/2026 |
| zapier.com | Zapier | <https://zapier.com/pricing> | 11/11/2026 |
