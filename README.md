```markdown
# 🚀 Infrastructure Virtuelle Vagrant + VirtualBox

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-plain.svg" alt="Bootstrap CSS" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-original.svg" alt="Ruby" width="40" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vagrant/vagrant-original.svg" alt="Vagrant" width="40" height="40" />
</p>

---

## Sommaire

- [Installation](#installation)
- [Travaux Pratiques](#travaux-pratiques)
- [Étape 1 – Création d’une box Debian (base)](#étape-1--création-dune-box-debian-base)
- [Livrables](#livrables)

---

## Installation

### Installation de VirtualBox sur Ubuntu 25.04 / Debian 13

```

sudo apt update \&\& sudo apt upgrade -y
sudo apt install -y dkms build-essential linux-headers-\$(uname -r)
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian \$(lsb_release -cs) contrib"
sudo apt update
sudo apt install -y virtualbox-7.0
virtualbox --help

```

### Installation de Vagrant

```

curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com \$(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update
sudo apt install -y vagrant
vagrant --version

```

---

## Travaux Pratiques

Objectif : Mettre en place progressivement une infrastructure virtuelle utilisant Vagrant + VirtualBox pour comprendre :

- La notion de box
- La création d’une VM automatisée
- Le provisionnement
- Les dossiers partagés
- La modélisation multi-VM (séparation web / base de données)

Le projet se déroule en 3 étapes, validant chacune des compétences techniques.

---

## Étape 1 – Création d’une box Debian (base)

### Cahier des charges

- Projet `tp-vagrant-debian`
- Vagrantfile minimal utilisant la box `bento/debian-13`
- Configuration VM :
  - Nom : `debian-base`
  - Provider VirtualBox :
    - RAM : 1024 Mo
    - CPU : 1
    - Réseau privé avec IP fixe `192.168.56.10`
- Fonctionnalités :
  - VM lancée avec `vagrant up`
  - Accès SSH via `vagrant ssh`
  - Message personnalisé dans `/etc/motd` au provisionnement (ex : `"VM TP – Debian Base"`)

---

## Livrables

- Dossier `tp-vagrant-debian` dans GitHub
- Contenu : `Vagrantfile` suivant le cahier des charges

---

Merci de consulter ce README pour un guide clair et concis.  
Bonne mise en place de votre environnement Vagrant et VirtualBox ! 🚀
```

Cette mise en forme améliore la lisibilité, valorise chaque section et facilite la navigation grâce au sommaire. L’intégration des icônes est centrée et aérée visuellement. Les blocs de code sont bien délimités pour faciliter la copie et l'exécution des commandes.

N’hésitez pas à demander si vous souhaitez un exemple complet de Vagrantfile pour l’étape 1.
<span style="display:none">[^1][^2][^3][^4][^5][^6][^7][^8][^9]</span>

<div align="center">⁂</div>

[^1]: https://github.com/patrickdlee/vagrant-examples

[^2]: https://github.com/vdmitriyev/vagrant-templates

[^3]: https://github.com/lukmanlab/vagrant-virtualbox

[^4]: https://vagrant-libvirt.github.io/vagrant-libvirt/examples.html

[^5]: https://www.cisco.com/c/fr_ca/support/docs/cloud-systems-management/iox/222392-build-iox-apps-with-vagrant-and-virtualb.html

[^6]: https://www.craigthacker.dev/blog/dev-env-p1

[^7]: http://tvaira.free.fr/bts-sn/admin/Creation-Box-Vagrant.pdf

[^8]: https://www.devuniversity.com/blog/vagrant-installe-automatise-machines-virtuelles

[^9]: https://aquasecurity.github.io/tracee/v0.7.0/tutorials/setup-development-machine-with-vagrant/

