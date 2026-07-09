# Sigma Rules — Windows Detection Lab

Ce dépôt contient des règles Sigma rédigées à partir d’exercices de détection Windows :  

- rédaction de règles Sigma lisibles ;
- détection comportementale Windows ;
- mapping MITRE ATT&CK ;
- distinction entre indicateurs CTF et comportements réutilisables ;
- documentation des faux positifs ;
- amélioration progressive des règles.

## Périmètre

Les règles couvrent principalement :

- création de processus Windows ;
- abus de LOLBins ;
- téléchargement de payload ;
- persistance ;
- exécution PowerShell suspecte ;
- staging d’archives ;
- exfiltration HTTP ;
- indicateurs spécifiques au CTF SigHunt.

## Structure du dépôt

```text
sigma-rules/
├── README.md
├── rules/
│   ├── windows/
│   │   ├── process_creation/
│   │   │   ├── proc_creation_win_mshta_spawned_by_browser.yml
│   │   │   ├── proc_creation_win_certutil_download_binary.yml
│   │   │   ├── proc_creation_win_netcat_cmd_execution.yml
│   │   │   ├── proc_creation_win_powershell_powerup_invoke_allchecks.yml
│   │   │   ├── proc_creation_win_sc_config_suspicious_binpath.yml
│   │   │   ├── proc_creation_win_reg_runonce_suspicious_persistence.yml
│   │   │   ├── proc_creation_win_7zip_password_archive_staging.yml
│   │   │   └── proc_creation_win_curl_http_exfiltration.yml
│   │   └── file_event/
│   │       └── file_event_win_sighunt_huntme_marker.yml
│   └── ctf/
│       └── tryhackme_sighunt/
│           └── original_notes.md
└── docs/
    └── sighunt_detection_notes.md
