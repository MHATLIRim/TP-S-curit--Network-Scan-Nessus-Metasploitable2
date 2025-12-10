# 🛡️ TP Scan Réseau & Analyse de Vulnérabilités (Nessus & Metasploitable2)

##  Objectifs
- Scanner un réseau local avec Nmap
- Installer et configurer Nessus Essentials sur Kali Linux
- Détecter les vulnérabilités de Metasploitable2
- Documenter et analyser les vulnérabilités pour le TP

---

## 🛠️ Outils Utilisés
- Kali Linux (192.168.157.135)
- Metasploitable2 (192.168.157.133)
- Nessus Essentials
- Nmap
- VMware Workstation / Fusion

---

## 📡 Configuration Réseau

| Machine          | IP              | Rôle       |
|-----------------|----------------|-----------|
| Kali Linux       | 192.168.157.135 | Attaquant |
| Metasploitable2  | 192.168.157.133 | Cible     |

- Les deux machines sont sur le même réseau NAT/Bridged pour permettre la communication.

---

## 🚀 Étapes Réalisées

1. Installation de Nessus Essentials sur Kali
2. Activation avec licence Essentials
3. Création d’un utilisateur administrateur via CLI
4. Vérification des IP et connectivité avec `ping`
5. Scan réseau avec Nmap
6. Scan de vulnérabilités avec Nessus (Basic Network Scan)
7. Analyse et documentation des résultats

---

##  Commandes Importantes (commands.txt)

```bash
# Vérification des IP
ifconfig        # Kali / Metasploitable2
ip a            # Alternative
ping -c 4 192.168.157.133  # Ping Metasploitable2 depuis Kali

# Mise à jour Kali
sudo apt update && sudo apt full-upgrade -y

# Scan Nmap
nmap 192.168.157.133       # Scan simple
nmap -p- 192.168.157.133   # Tous les ports
nmap -O 192.168.157.133    # Détection OS
nmap -p 22,443 192.168.157.133  # Vérifier SSH et HTTPS

# Nessus
sudo systemctl start nessusd
sudo /opt/nessus/sbin/nessuscli adduser  # Ajouter admin si besoin
# Scan dans l’interface web → Basic Network Scan → Cible : 192.168.157.133
