# ansibleProject
This project deploy the bootcamp app by ansible.
The link for the github app: https://github.com/shir707/bootcamp-app.git

commands:

in order to run stage enviorment run:
ansible-playbook -v -i inventories/stage --extra-vars server_env_group="stageServers" main.yml

in order to run prod enviorment run:
ansible-playbook -v -i inventories/prod --extra-vars server_env_group="prodServers" main.yml

checking:
In the web browser(prod env): 
http://52.149.172.80:8080/list

In the web browser(stage env):
http://20.37.134.76:8080/list

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
