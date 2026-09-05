L'arborescence du projet

Créer un dossier group_vars à l'intérieur vous allez mettre 2 dossiers dont chancun aura des variable et un fichier vault pour les secrets initialiser le vault pour sécuriser vos variables 
.
├── ansible.cfg
├── inventories
│   ├── group_vars
│   │   ├── managers
│   │   │   ├── vars.yml
│   │   │   └── vault.yml
│   │   └── workers
│   │       ├── vars.yml
│   │       └── vault.yml
│   ├── hosts
│   └── host_vars
├── playbooks
│   ├── deploy.yml
│   ├── docker.yml
│   ├── install.yml
│   ├── manager.yml
│   ├── uninstall.yml
│   └── workers.yml
├── README.md
└── roles
    ├── common
    │   └── tasks
    │       └── main.yml
    ├── deploy
    │   ├── files
    │   │   ├── certs
    │   │   ├── edge
    │   │   │   └── docker-compose.edge.yml
    │   │   ├── netflix
    │   │   │   └── docker-compose.prod.yml
    │   │   ├── nginx.conf
    │   │   ├── rpn
    │   │   │   └── docker-compose.prod.yml
    │   │   └── traefik
    │   │       ├── config
    │   │       │   └── traefik.yaml
    │   │       └── docker-compose.yml
    │   └── tasks
    │       ├── edge.yml
    │       ├── main.yml
    │       ├── netflix.yml
    │       ├── rpn.yml
    │       └── traefik.yml
    ├── docker
    │   └── tasks
    │       └── main.yml
    ├── swarm
    │   └── tasks
    │       └── main.yml
    ├── uninstall
    │   └── tasks
    │       └── main.yml
    └── worker
        └── tasks
            └── main.yml
