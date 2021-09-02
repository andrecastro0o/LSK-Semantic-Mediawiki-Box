# LSK - Semantic Mediawiki in a Vagrant Box

Github mirror: https://github.com/TIBHannover/LSK-Semantic-Mediawiki-Box


(IN PROGRESS)

**Installs [Mediawiki](https://www.mediawiki.org/wiki/MediaWiki) and [Semantic Mediawiki(SMW)](https://www.semantic-mediawiki.org) in Vagrant box**

* Mediawiki version: 1.35 current long-term support (LTS)
* Semantic Mediawiki version: 3.2.3


Requirements to run box:
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


## Installation

Run the following steps in Terminal (Linux/macOS) or GitBash (Windows):
```bash
git clone git@git.tib.eu:lab-linked-scientific-knowledge/semantic-mediawiki-box.git
cd semantic-mediawiki-box
vagrant up
```

## View

Wiki User:
* user name: `Admin`
* user password: `AdminPWD`


**TODO**
* mirror to github
* 


After installation process has finished, **visit Fuseki UI at  <http://192.168.60.120/??/??/>**

`vagrant reload --provision` will re-run the Ansile playbook in the created Vagrant box

## Stop and Restart

It is possible to shut down the virtual box and restart it again in order to save CPU and RAM.

```bash
# shut down
vagrant halt

# restart
vagrant reload --provision
```

In order to suspend the virtual box (save the state) use suspend and resume.

```bash
# save the state to disc
vagrant suspend

# resume from disc
vagrant resume
```

# For Deployment:
* look for default/main.yml vars with `# IN DEPLOYMENT: overwrite in host file` and write them in hosts file of deployment repos


# TODO
