Scan de Vulnérabilités avec Nessus & Metasploitable 2

 Objectif
Réaliser un scan de vulnérabilités avec Nessus Essentials sur la machine Metasploitable 2.

Outils Utilisés
- Kali Linux
- Nessus Essentials
- Metasploitable 2 (Machine vulnérable)
- VirtualBox / VMware

 Configuration Réseau
| Machine | IP | Rôle |
|---------|----|-----|
| Kali Linux | 192.168.157.135 | Attaquant |
| Metasploitable 2 | 192.168.157.133 | Cible |

 Étapes Réalisées
1. Installation de Nessus sur Kali
2. Enregistrement de la licence Essentials
3. Création d’un administrateur
4. Scan de la machine Metasploitable 2
5. Analyse des vulnérabilités découvertes


Principales Vulnérabilités Trouvées (quelques vulnérabilités)
| Vulnérabilité | Gravité | Port |
|--------------|---------|------|
| Backdoor | Critique | 20 |
|web servers |  High | 10 |
Low |service detection| 6


*Nessus a identifié plusieurs vulnérabilités critiques permettant une prise de contrôle distante de la machine cible.*
