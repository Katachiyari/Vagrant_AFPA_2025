```markdown
# 🚀 Infrastructure Virtuelle Vagrant + VirtualBox

<!-- Icônes des technologies -->
<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-plain.svg" alt="Bootstrap CSS" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-original.svg" alt="Ruby" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vagrant/vagrant-original.svg" alt="Vagrant" width="40" height="40" />
</p>

---

## Installation

### Installation de VirtualBox sur Ubuntu 25.04 / Debian 13

```


# Mise à jour des paquets

sudo apt update \&\& sudo apt upgrade -y

# Installation des dépendances de VirtualBox

sudo apt install -y dkms build-essential linux-headers-\$(uname -r)

# Ajout du dépôt VirtualBox

wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian \$(lsb_release -cs) contrib"

# Installation de VirtualBox

sudo apt update
sudo apt install -y virtualbox-7.0

# Vérification de l'installation

virtualbox --help

```

### Installation de Vagrant

Selon la documentation officielle Vagrant pour Ubuntu / Debian :

```


# Ajouter la clé publique Hashicorp

curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

# Ajouter le dépôt officiel

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com \$(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

# Installation de Vagrant

sudo apt update
sudo apt install vagrant

# Vérification de l'installation

vagrant --version

```

---

## Travaux Pratiques : Infrastructure Virtuelle Progressive

Mise en place d’une infrastructure virtuelle Vagrant + VirtualBox pour comprendre :

- La notion de box
- La création automatisée d’une VM
- Le provisionnement
- Les dossiers partagés
- La modélisation multi-VM (séparation web / base de données)

Le projet se déroule en 3 étapes, chacune validant des compétences techniques.

---

## Étape 1 – Création d’une box Debian (base)

### Cahier des charges

Créer un projet Vagrant nommé `tp-vagrant-debian` contenant :

- Un `Vagrantfile` minimal utilisant la box : `bento/debian-13`
- Configuration demandée :
  - Nom de la VM : `debian-base`
  - Provider VirtualBox :
    - RAM : 1024 Mo
    - CPU : 1
    - Réseau privé avec IP fixe : `192.168.56.10`

La VM doit :

- Se lancer avec `vagrant up`
- Être accessible en SSH via `vagrant ssh`
- Afficher un message personnalisé dans `/etc/motd` au provisionnement, par exemple :  
  `"VM TP – Debian Base"`

---

## Livrables

Un dossier GitHub `tp-vagrant-debian` contenant :

- `Vagrantfile` correspondant au cahier des charges

---

Merci de suivre ces instructions et de valider chaque étape par vos livrables. Bon travail avec Vagrant et VirtualBox ! 🚀
```

Si vous souhaitez, je peux vous aider à créer un exemple de `Vagrantfile` pour cette étape aussi.


