# logos_platform

A web app for symbolic intelligence training, created for personal learning purposes. The core idea is to allow the user to insert data about themself and get insights from the app. A self-hacking app.

The core idea is to build a full-stack web application using Prolog as the backend language, leveraging its stengths in symbolic reasoning and knowledge representation. The frontend is built with standard web technologies (HTML, CSS, JavaScript) to provide a user-friendly interface.

Copyright (C)  2025  porcielf.
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3
    or any later version published by the Free Software Foundation;
    with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
    A copy of the license is included in the section entitled "GNU
    Free Documentation License".

## Directory Tree

```
project-root/
├─ README.md
├─ LICENSE
├─ .gitignore
├─ docs/
│  ├─ architecture.md
│  ├─ api-contracts.md
│  ├─ security-model.md
│  └─ data-model.md
├─ config/
│  ├─ server.env
│  ├─ storage.env
│  └─ settings.pl
├─ frontend/
│  ├─ public/
│  │  ├─ index.html
│  │  ├─ favicon.ico
│  │  ├─ manifest.json
│  │  └─ robots.txt
│  ├─ assets/
│  │  ├─ css/
│  │  │  ├─ base.css
│  │  │  ├─ layout.css
│  │  │  ├─ theme.css
│  │  │  └─ components/
│  │  │     ├─ header.css
│  │  │     ├─ footer.css
│  │  │     └─ cards.css
│  │  ├─ js/
│  │  │  ├─ main.js
│  │  │  ├─ api/
│  │  │  │  ├─ client.js
│  │  │  │  └─ endpoints.js
│  │  │  ├─ ui/
│  │  │  │  ├─ dom.js
│  │  │  │  └─ components/
│  │  │  │     ├─ modal.js
│  │  │  │     └─ table.js
│  │  │  └─ utils/
│  │  │     ├─ validators.js
│  │  │     └─ formatters.js
│  │  ├─ img/
│  │  │  └─ ...
│  │  └─ fonts/
│  └─ pages/
│     ├─ home.html
│     ├─ dashboard.html
│     └─ settings.html
├─ backend/
│  ├─ server/
│  │  ├─ app.pl
│  │  ├─ routes/
│  │  │  ├─ http_routes.pl
│  │  │  └─ ws_routes.pl
│  │  ├─ middleware/
│  │  │  ├─ auth_guard.pl
│  │  │  ├─ rate_limit.pl
│  │  │  └─ audit_log.pl
│  │  ├─ adapters/
│  │  │  ├─ http_adapter.pl
│  │  │  └─ ws_adapter.pl
│  │  └─ handlers/
│  │     ├─ query_handler.pl
│  │     ├─ mutation_handler.pl
│  │     └─ stream_handler.pl
│  ├─ knowledge/
│  │  ├─ facts/
│  │  │  ├─ users.pl
│  │  │  ├─ roles.pl
│  │  │  ├─ permissions.pl
│  │  │  └─ domain_entities.pl
│  │  ├─ rules/
│  │  │  ├─ business_rules.pl
│  │  │  ├─ inference_rules.pl
│  │  │  └─ security_policies.pl
│  │  ├─ ontologies/
│  │  │  ├─ schema.pl
│  │  │  └─ taxonomy.pl
│  │  └─ datasets/
│  │     └─ seed_data.pl
│  ├─ inference/
│  │  ├─ engine.pl
│  │  ├─ reasoning/
│  │  │  ├─ forward_chaining.pl
│  │  │  ├─ backward_chaining.pl
│  │  │  └─ constraint_solving.pl
│  │  └─ query_language/
│  │     ├─ dsl_parser.pl
│  │     └─ translator.pl
│  ├─ security/
│  │  ├─ theorematic/
│  │  │  ├─ proofs.pl
│  │  │  ├─ policy_models.pl
│  │  │  └─ verification.pl
│  │  ├─ auth/
│  │  │  ├─ credentials.pl
│  │  │  ├─ tokens.pl
│  │  │  └─ session.pl
│  │  └─ integrity/
│  │     ├─ checksums.pl
│  │     └─ tamper_detection.pl
│  ├─ storage/
│  │  ├─ intelligent_store.pl
│  │  ├─ persistence/
│  │  │  ├─ snapshot.pl
│  │  │  ├─ append_log.pl
│  │  │  └─ backup_restore.pl
│  │  ├─ indexing/
│  │  │  ├─ btree.pl
│  │  │  └─ fulltext.pl
│  │  └─ caching/
│  │     ├─ memoization.pl
│  │     ├─ lru_cache.pl
│  │     └─ cache_invalidation.pl
│  ├─ integration/
│  │  ├─ serializers/
│  │  │  ├─ json.pl
│  │  │  └─ csv.pl
│  │  ├─ transport/
│  │  │  ├─ http.pl
│  │  │  └─ websocket.pl
│  │  └─ adapters/
│  │     └─ frontend_bridge.pl
│  └─ tests/
│     ├─ unit/
│     │  ├─ inference_engine_tests.pl
│     │  ├─ storage_tests.pl
│     │  └─ security_tests.pl
│     ├─ integration/
│     │  ├─ api_contract_tests.pl
│     │  └─ end_to_end_tests.pl
│     └─ fixtures/
│        └─ sample_data.pl
├─ scripts/
│  ├─ dev_run.sh
│  ├─ build.sh
│  ├─ seed.sh
│  └─ test.sh
└─ deployment/
   ├─ docker/
   │  ├─ Dockerfile.prolog
   │  └─ nginx.conf
   ├─ compose/
   │  └─ docker-compose.yml
   └─ k8s/
      ├─ deployment.yml
      └─ service.yml
```
