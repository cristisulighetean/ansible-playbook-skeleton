# Ansible Playbook Skeleton

This should be the starting point for any Ansible Playbook project. It will contain the basic project structure.

## Basic project structure

```py
├── defaults                # Variables with the lowest precedence
│   └── main.yml
│
├── handlers                # Special tasks that run at the end of a play if notified
│   └── main.yml
│
├── meta                    # Information about the role for Ansible Galaxy
│   └── main.yml
│
├── molecule                # Used for testing the role in isolated environments
│   └── default             # Default Molecule scenario
│       ├── converge.yml
│       └── molecule.yml
│
├── tasks                   # Contains the main list of tasks to be executed by the role
│   ├── task1.yaml
│   └── task2.yaml
│
├── templates               # Jinja2 templates for generating configuration files
│   └── template.j2
│
├── vars
│   └── vars.yml            # High precedence variables, typically platform-specific
│
├── ansible.cfg            # Ansible configuration file
├── inventory              # Directory for inventory files
│   ├── hosts.ini          # Main inventory file
│   └── group_vars         # Group specific variables
│       ├── group1.yml
│       └── group2.yml
│
├── roles                  # Roles directory
│   ├── role1              # Specific role directory
│   │   ├── defaults       # Default variables for the role
│   │   │   └── main.yml
│   │   ├── handlers       # Handlers for the role
│   │   │   └── main.yml
│   │   ├── tasks          # Tasks for the role
│   │   │   └── main.yml
│   │   ├── templates      # Jinja2 templates for configuration files
│   │   └── vars           # Other variables for the role
│   │       └── main.yml
│   └── role2
│       ...
│
├── main.yaml   # Initial  # Entry point for the playbook
│
└── README.md              # Project documentation

```