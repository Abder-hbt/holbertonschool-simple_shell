
<p align="center">
    <img src="https://raw.githubusercontent.com/Abder-hbt/holbertonschool-simple_shell/refs/heads/main/LOGO_SHELL_SF.png" alt="Logo SHELL" style="width: 500px;">
</p>

# Sommaire
- [Description](#1.-Description)
- [Structure des fichiers](#structure-des-fichiers)
- [Appels système et bibliothèques](#appels-système-et-bibliothèques)
- [Installation](#installation)
- [Example d'uilisation](#example-d'utilisation)
- [Contributions](#contributions)
- [Auteurs](#auteurs)

# Project SHELL
Ce projet consiste à recréer un shell Unix simplifié en langage C. Le shell permettra d'exécuter des commandes comme `ls` ou `pwd`, de gérer les arguments, de créer des processus avec `fork()`, et d'utiliser les variables d'environnement pour localiser les programmes. Il inclura une boucle interactive pour saisir et exécuter des commandes, tout en gérant les erreurs et en appliquant les concepts fondamentaux des systèmes Unix, comme les appels système et la gestion des processus.

---

## 1. Description
Le Simple Shell est un interprète de commandes UNIX simple, entièrement écrit en C. Le programme fonctionne à partir des commandes bash saisies via l'interface en ligne de commande (CLI) par l'utilisateur. Tout texte séparé par un nombre quelconque d'espaces, de tabulations ou une combinaison des deux est considéré comme un argument. La commande correspondante saisie par l'utilisateur est ensuite analysée et exécutée comme dans un shell UNIX classique.  

**Cycle de vie basique d'un shell :**  
1. Lancer le shell  
2. Attendre une entrée de l'utilisateur  
3. Analyser l'entrée de l'utilisateur  
4. Exécuter la commande et retourner le résultat  
5. Revenir à l'étape 2  

* Vous pouvez terminer le shell à tout moment en tapant la commande `exit` dans l'invite de commande ou en utilisant `Ctrl-D`, qui est interprété comme un End-of-File (EOF).  
