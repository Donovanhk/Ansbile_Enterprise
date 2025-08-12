```text
ansible-enterprise/
├── 🔸inventories/              # Convention (not auto-recognized unless configured)
│   ├── production/
│   │   ├── 🔸hosts             # Inventory file (INI or YAML)
│   │   └── 🔸group_vars/       # Auto-loaded group variables
│   │       └── windows_all.yml
│   ├── staging/
│   │   ├── hosts
│   │   └── group_vars/
│   └── development/
│       ├── hosts
│       └── group_vars/
│
├── 🔸roles/                    # Auto-recognized role directory
│   └── windows_updates/
│       ├── 🔸tasks/            # Required for role execution
│       │   └── main.yml
│       ├── 🔸vars/             # Static variables
│       │   └── main.yml
│       ├── 🔸defaults/         # Lowest precedence variables
│       │   └── main.yml
│       ├── 🔸handlers/         # Notification handlers
│       │   └── main.yml
│       ├── 🔸templates/        # Jinja2 templates
│       ├── 🔸files/            # Static files
│       └── README.md
│
├── playbooks/                 # Convention (not auto-recognized)
│   ├── windows.yml
│   └── linux.yml
│
├── site.yml                   # Main playbook (name is conventional)
├── 🔸ansible.cfg              # Auto-loaded config file
├── requirements.yml      # Optional: for role dependencies
└── README.md

