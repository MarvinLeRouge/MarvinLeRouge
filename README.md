[🇫🇷 Version française](#jean-ceugniet-développeur-backend--data-engineer) | [🇬🇧 English version](#jean-ceugniet-backend-developer--data-engineer)

# Jean Ceugniet, Développeur Backend / Data Engineer

**15+ ans de backend**, et un faible pour les traitements trop lents et les données en désordre. J'ai notamment ramené **de plus de 3 minutes à moins de 5 secondes** un module qu'on croyait cassé, alors qu'il était juste désespérément lent. Je construis des **pipelines de données fiables**, et je monte en compétences sur la **stack Data Engineering moderne** (orchestration, modélisation analytique).

🌐 **[MarvinLeRouge.dev](https://marvinlerouge.dev)** (fiches projet) | 👔 **[LinkedIn](https://www.linkedin.com/in/jean-ceugniet/)** | 📧 **[jean.ceugniet@gmail.com](mailto:jean.ceugniet@gmail.com)**

## 🧭 Démarche qualité

### [Engineering-Radar](https://github.com/MarvinLeRouge/Engineering-Radar)
Suivi de la qualité de mes dépôts, fondé sur des preuves. Tous les projets ci-dessous y passent.
- Plus de 20 outils d'analyse reconnus
- Référentiel de scoring versionné
- Constats priorisés par criticité
- Ré-audits qui mesurent les progrès réels

## 📊 Projets data

### [JobFlow](https://github.com/MarvinLeRouge/JobFlow), en production
Pipeline Python qui ingère les alertes emploi de sept fournisseurs, depuis Gmail, vers un Google Sheet unique et dédupliqué.
- Cinq étapes exécutables isolément, enchaînées par un orchestrateur qui s'arrête à la première erreur
- Chargement incrémental piloté par un registre d'état
- Déduplication entre fournisseurs
- Garde-fou qui bloque la synchronisation tant qu'une erreur n'a pas été acquittée

### [geo_data](https://github.com/MarvinLeRouge/geo_data)
Pipeline de téléchargement de limites administratives publiques et de corrélation entre sources.
- Sources : INSEE, geoBoundaries, GeoNames
- Sortie GeoJSON normalisée par pays et par niveau administratif, données brutes conservées
- Contrat de sortie versionné et documenté
- Consommé en production par GeoChallenge-Tracker

## 🗺️ Applications

### [GeoChallenge-Tracker](https://github.com/MarvinLeRouge/GeoChallenge-Tracker)
Application web (FastAPI, MongoDB, Vue.js 3) qui suit la progression des challenges de géocaching, à partir des trouvailles importées en GPX.
- API de plus de 70 endpoints, architecture hexagonale
- Règles de challenge décrites comme des arbres d'expression, compilés en requêtes MongoDB
- Recherches par zone sur index géospatial
- Audit de sécurité OWASP Top 10 / ASVS, toutes les remarques corrigées
- Tests utilisateurs menés avec une équipe de géocacheurs expérimentés, aux profils et aux pratiques variés

### [Summit-Stats](https://github.com/MarvinLeRouge/Summit-Stats)
Application web (Laravel, PostgreSQL, Vue.js 3) d'analyse de traces GPS de randonnée.
- Pipeline d'analyse développé en TDD : parsing, enrichissement d'altitude, lissage, segmentation par pente
- Métriques dérivées sur séries temporelles (vitesse verticale, vitesse en mouvement, répartition par pente)
- Audit de sécurité OWASP Top 10 / ASVS et durcissement de l'API
- Déploiement continu, seuil de couverture bloquant en CI

## ⚡ Optimisation en production

Sur une plateforme SaaS de veille documentaire, base MySQL de 1 To (8 schémas, plus de 1000 tables) :

- **x37** : de plus de 3 minutes à moins de 5 secondes pour le comptage des éléments liés à chaque ligne d'une liste de résultats. Les traitements redondants ont été supprimés et une requête générique non indexable a été remplacée par des requêtes spécifiques. Les deux versions ont tourné en parallèle en production avant la bascule.
- **-80 %** sur le temps SQL global d'un autre module, au terme d'une analyse approfondie des logs SQL pour traquer les appels répétés, puis d'une réécriture extensive des requêtes, dont le nombre a été divisé par 33.
- **Audit de la base** : recherche des anomalies de structure et de performance des index (EXPLAIN ANALYZE, slow query log, performance_schema, logs SQL), puis étude et test de plusieurs solutions, dont les index composites et le partitionnement, et proposition d'un plan de transition.

## 🛠️ Compétences

- **Backend et API** : Python, FastAPI, PHP, Laravel, NestJS, Fastify, API REST, OpenAPI
- **Bases de données** : MySQL (10+ ans en production), PostgreSQL, MongoDB, SQLite, Redis ; optimisation de requêtes, indexation, migrations versionnées
- **Data** : pipelines d'ingestion, chargement incrémental, déduplication, data contract, validation de schéma, GeoJSON, séries temporelles
- **Qualité et infrastructure** : architecture hexagonale, TDD, pytest, Pest, Vitest, Playwright, Docker, Traefik, GitHub Actions, Linux
- **Frontend** : Vue.js 3, TypeScript, Tailwind CSS, Leaflet
- **Accessibilité** : audits RGAA et WCAG

**Enseignement** : 4 ans de vacations en développement web à l'IUT MMI de Toulon, plus de 200 étudiants.

## 🔥 Montée en compétences

Parcours structuré d'auto-formation en Data Engineering, mené en parallèle de mes projets.
- **Méthode** : une compétence n'est acquise qu'avec une preuve à l'appui (exercice, lab ou projet)
- **Point de départ** : bilans initiaux en SQL, bases de données et Python
- **En cours** : SQL avancé (fonctions de fenêtrage) et optimisation
- **Au programme** : modélisation de données, ETL / ELT, entrepôt de données, dbt, orchestration, qualité des données
- **Ensuite** : Spark, Kafka, cloud

## 🎯 Ouvert aux opportunités

Développement backend Python, développement orienté données, Data Engineering. Basé à Toulon, ouvert au remote.

---

# Jean Ceugniet, Backend Developer / Data Engineer

**15+ years of backend development**, and a soft spot for slow processes and messy data. Among other things, I took a module thought to be broken, when it was just painfully slow, **from over 3 minutes down to under 5 seconds**. I build **reliable data pipelines**, and I'm currently upskilling on the **modern Data Engineering stack** (orchestration, analytical modeling).

🌐 **[marvinlerouge.dev](https://marvinlerouge.dev)** (project write-ups) | 👔 **[LinkedIn](https://www.linkedin.com/in/jean-ceugniet/)** | 📧 **[jean.ceugniet@gmail.com](mailto:jean.ceugniet@gmail.com)**

## 🧭 Quality approach

### [Engineering-Radar](https://github.com/MarvinLeRouge/Engineering-Radar)
Evidence-based quality tracking for my repositories. Every project below goes through it.
- Over 20 established analysis tools
- Versioned scoring framework
- Findings prioritized by severity
- Re-audits that measure real progress

## 📊 Data projects

### [JobFlow](https://github.com/MarvinLeRouge/JobFlow), in production
Python pipeline that ingests job alerts from seven providers, from Gmail into a single, deduplicated Google Sheet.
- Five independently runnable stages, chained by an orchestrator that stops at the first error
- Incremental loading driven by a state ledger
- Cross-provider deduplication
- Gate that blocks the sync until any error has been acknowledged

### [geo_data](https://github.com/MarvinLeRouge/geo_data)
Pipeline that downloads public administrative boundaries and joins them across sources.
- Sources: INSEE, geoBoundaries, GeoNames
- GeoJSON output normalized by country and administrative level, raw data kept
- Versioned, documented output contract
- Consumed in production by GeoChallenge-Tracker

## 🗺️ Applications

### [GeoChallenge-Tracker](https://github.com/MarvinLeRouge/GeoChallenge-Tracker)
Web application (FastAPI, MongoDB, Vue.js 3) that tracks geocaching challenge progress from finds imported as GPX.
- API with over 70 endpoints, hexagonal architecture
- Challenge rules described as expression trees, compiled into MongoDB queries
- Area searches on a geospatial index
- OWASP Top 10 / ASVS security audit, every finding fixed
- User testing with a team of experienced geocachers, with varied profiles and playing styles

### [Summit-Stats](https://github.com/MarvinLeRouge/Summit-Stats)
Web application (Laravel, PostgreSQL, Vue.js 3) for hiking GPS track analysis.
- Analysis pipeline built test-first: parsing, elevation enrichment, smoothing, slope segmentation
- Derived time-series metrics (vertical speed, moving speed, slope breakdown)
- OWASP Top 10 / ASVS security audit and API hardening
- Continuous deployment, blocking coverage threshold in CI

## ⚡ Production optimization

On a document-monitoring SaaS platform, 1 TB MySQL database (8 schemas, 1000+ tables):

- **x37**: from over 3 minutes to under 5 seconds to count the items linked to each row of a result list. Redundant processing was removed and a non-indexable generic query was replaced with specific queries. Both versions ran in parallel in production before the switch.
- **-80%** on another module's overall SQL time, following an in-depth analysis of the SQL logs to track down repeated calls, then an extensive rewrite of the queries, whose number was divided by 33.
- **Database audit**: tracking down structural and index performance issues (EXPLAIN ANALYZE, slow query log, performance_schema, SQL logs), then studying and testing several solutions, including composite indexes and partitioning, and proposing a transition plan.

## 🛠️ Skills

- **Backend and APIs**: Python, FastAPI, PHP, Laravel, NestJS, Fastify, REST APIs, OpenAPI
- **Databases**: MySQL (10+ years in production), PostgreSQL, MongoDB, SQLite, Redis; query optimization, indexing, versioned migrations
- **Data**: ingestion pipelines, incremental loading, deduplication, data contracts, schema validation, GeoJSON, time series
- **Quality and infrastructure**: hexagonal architecture, TDD, pytest, Pest, Vitest, Playwright, Docker, Traefik, GitHub Actions, Linux
- **Frontend**: Vue.js 3, TypeScript, Tailwind CSS, Leaflet
- **Accessibility**: RGAA and WCAG audits

**Teaching**: 4 years as an adjunct lecturer in web development at IUT MMI Toulon, 200+ students.

## 🔥 Upskilling

A structured Data Engineering self-study path, run alongside my projects.
- **Method**: a skill only counts as acquired with evidence (exercise, lab or project)
- **Starting point**: initial assessments in SQL, databases and Python
- **In progress**: advanced SQL (window functions) and optimization
- **Next up**: data modeling, ETL / ELT, data warehousing, dbt, orchestration, data quality
- **Later**: Spark, Kafka, cloud

## 🎯 Open to opportunities

Python backend development, data-oriented development, Data Engineering. Based in Toulon, open to remote.

[⬆ Retour en haut / Back to top](#)
