# ansibleProject

commands:
ansible-playbook -v -i inventories/stage --extra-vars server_env_group="stageServers" main.yml


Structure:

.
├── inventories
│   ├── stage
│   │   ├── group_vars
│   │   │   └── stageServers.yml
│   │   └── host
│   └── prod
│       ├── group_vars
│       │   └── prodServers.yml
│       └── hosts
├── main.yml
└── roles
    └── common
        └── tasks
            └── main.yml
