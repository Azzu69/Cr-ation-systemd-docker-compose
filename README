# Création d'un fichier systemd pour un service docker compose

```ssh
nano /etc/systemd/system/nomduservice.service
```

Copier et modifier le code suivant :
```ssh
[Unit]
Description=Nom du service
Requires=docker.service
After=docker.service

[Service]
Type=oneshot
WorkingDirectory=/emplacement/des/fichiers
Environment=COMPOSE_HTTP_TIMEOUT=600
ExecStart=/usr/bin/env /usr/bin/docker-compose -f /route/du/docker-compose.yml up -d
ExecStop=/usr/bin/env /usr/bin/docker-compose -f /route/du/docker-compose.yml stop
StandardOutput=syslog
RemainAfterExit=yes

[Install]
WantedBy=multi-user.target
```
