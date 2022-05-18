# DevOps 2. časť

#### Ciele cvičenia
- Oboznámiť sa s nasadzovaním kontajnerizovanej aplikácie na platforme AWS
  - AWS ECS (orchestrácia) + AWS EC2 (server)
- Vybrať si cloud platformu (AWS, Digital Ocean, MS Azure, Google Cloud) a oboznámiť sa s jej službami týkajúcimi sa nasadzovania a orchestrácie SW kontajnerov
- Pripraviť sa na nasadenie vlastnej "dockerizovanej" aplikácie
  - Server (AdonisJS), Klient (QuasarJS), RDBMS databáza (Postgres, MariaDB, MySQL)

#### Prerekvizity
- Zostavené a funkčné Docker images server + PWA klient, pripravené na nasadenie
  - Konfigurovateľné premenné prostredia (ENV)
  - Zabezpečená perzistencia dát (RDBMS)

#### Návod na získanie kreditov pre Digital Ocean, MS Azure (GitHub Student Developer Pack)
1. Zaregistrujte si [GitHub Student Developer Pack](https://education.github.com/pack), využite univerzitnú @stuba mailovú adresu.
2. Dokončite registráciu na Digital Ocean (alebo MS Azure) a prihláste sa do služy.

#### Úloha č. 1: Oboznámte sa s nasadzovaním na platforme AWS ECS (Elastic Container Service)
V spolupráci s cvičiacim sa oboznámte s nasadzovaním kontajnerizovanej webovej aplikácie (klient, server, RDBMS databáza) na platformu AWS ECS.
- Vytvorenie ECS klastra (EC2 inštancia t3.micro + podporné služby)
- Definícia úlohy (task definition)
- Vytvorenie služby (ECS service)
- Nastavenie bezpečnostných skupín (security groups)

#### Úloha č. 2: Pripravte svoju aplikáciu na cloudové nasadenie:
Vyberte si niektorú cloud platformu (AWS, Digital Ocean, MS Azure, Google Cloud) a oboznámte sa s jej službami týkajúcimi sa nasadzovania a orchestrácie SW kontajnerov. Pripravte svoju aplikáciu na nasadenie v cloude:
- Zostavený Docker image pre server časť (AdonisJS) aj klienta (QuasarJS)
  - Konfigurovateľné premenné prostredia (ENV: HOST, PORT, API_URL...)
  - Funkčný produkčný build
- Perzistencia dát prostredníctvom RDBMS
  - Postgres, MySQL, MariaDB podľa preferencie
  - Nakonfigurované premenné prostredia pre RDBMS aj pre server časť vašej aplikácie (DB_connection)
  - Pomôcka (PostgreSQL): [Docker Hub: Postgres](https://hub.docker.com/_/postgres)