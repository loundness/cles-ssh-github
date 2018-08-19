# 📋 Présentation:

Ce README permet de comprendre la démarche pour rentrer les clés "ssh" afin d'éviter de renseigner ses identifiants à chaque modifs d'un repository.

On peut s'inspirer ce [ce site](https://git-scm.com/book/fr/v2/Git-sur-le-serveur-G%C3%A9n%C3%A9ration-des-cl%C3%A9s-publiques-SSH) pour avoir plus d'infos sur l'utilisation des clés "ssh".


## 🖥 Sur sa console:

* **Vérifier si vous avez une clé de renseignée:**
`$ cat ~/.ssh/id_rsa.pub` 

* Si oui on devrait avoir un résultat:`

`ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCiew3W+4ieWBpzUEXeHfIjpfcw1kLL9i/3cWirHufVQhJFGg.....et qui finit par l'adresse mail de son compte github'`**


* Si non il faut en générer une avec cette commande:`

`$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`**

* Puis copiez la clé '$ cat ~/.ssh/id_rsa.pub' et renseignez-la dans votre compte github.


## :octocat: Sur votre compte Git Hub:

* Sur votre compte principal, allez dans "Settings" puis dans "SSH and GPG Keys" puis dans "SSH Keys"  cliquez sur "New SSH Key" et copiez la clé, vous pouvez donnez un nom dans "Title" à cette clé et enregistrez-le tout.

* Maintenant lorsque vous copiez un projet il faut sélectionner "SSH" et clonez "git remote add origin git@github.com:monnom/projet.git"

* Lors du premier push git vous demande le mot de passe de votre compte et après il n'y a plus qu'à faire un "push origin master" et ça roule


1. Une puce

2. Une puce bis

  `1 Une sous-puce`
  `2 Une sous-puce bis`
3. Une troisieme puce
