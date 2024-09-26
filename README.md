## HowMuchPaper
Old School Copier needs more paper before they running out!


## How to Run the Code: DON'T
Ensure you have the wolframalpha Python package installed:

      pip install wolframalpha

Replace YOUR_APP_ID with your actual WolframAlpha API key.
Run the script, and it will output the required number of cases of paper based on the number of working days.


## Goals
TBD
### HowMuchPaper_directory/

      ├── app/                        # Flask app files
      │   ├── app.py                  # Flask app main code
      │   ├── watchdog_script.py      # Watchdog script for auto-reload
      │   ├── requirements.txt        # Python dependencies
      │   ├── Dockerfile              # Dockerfile for the Flask app
      │   └── templates/              # HTML templates
      ├── docker-compose.yml          # Docker Compose config
      ├── ansible/                    # Ansible folder
      │   ├── playbook.yml            # Main playbook to deploy the app
      │   └── roles/                  # Ansible roles (tasks)
      │       └── flask_app/          # Role to deploy Flask app
      │           ├── tasks/          # Role tasks
      │           │   ├── main.yml    # Task to deploy Docker, app
      │           └── files/          # App files (if needed)
      └── hosts                       # Inventory file with server info

y
