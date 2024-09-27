## Simms's HowMuchPaper
Old School Copier needs more paper before they running out!

With a fleet of printers always buying paper is a pain.
The goal is to get to know how much paper you need. 


## ⬇️ How to Run the Code: DON'T
Ensure you have the wolframalpha Python package installed:

      docker-compose up --build

Replace YOUR_APP_ID with your actual WolframAlpha API key.
Run the script, and it will output the required number of cases of paper based on the number of working days.


## 💡 Goals

The aim is to find out the Monday - Friday paper use based on numbers reported by printers

      As this information can be found in many ways will build to meet my needs but also to just work*
      
            Ideally being able to pull from SNMP and get rolling number would be great
            
            But know the buffer
                  * How does it take to get more paper
                  * How much does need shif in a year


TBD
## 📜 Structure

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

## 💖 Support

If you find HowMuchPaper helpful, please consider giving it a ⭐️ to show your support!


## 🏅 Thanks to All Contributors

Thank you to everyone who has contributed to the development of Linutil. Your efforts are greatly appreciated, and you’re helping make this tool better for everyone!

[![Contributors]((https://contrib.rocks/image?repo=3aruin/HowMuchPaper))](https://github.com/3aruin/HowMuchPaper/graphs/contributors)
