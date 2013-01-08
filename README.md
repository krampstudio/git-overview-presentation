git-overview-presentation
=========================

French overview/presentation of GIT

#Plan:

## Retour d'expérience, pourquoi  je me suis intéressé à GIT 

### Context
 
 * 2009, chez un éditeur de soft
 * produit sous SVN 
 * versions custom par client
 * différentes versions en parallèle à maintenir
 * différents modules
 * différents sites/équipes de dev (LU, FR, ZA, SP) + off line (on site debug)
 
### Mise en place

 * workflow basé sur des features-branches
 * Maintenance sur des long term branches
 * Roles d'intégrateurs

### Constat

 * Premières semaines difficle pour les nons teckos, mais réglé par une formation interne d'une demi journée
 * Outils s'adapte aux processus (et non l'inverse)
 * Productivité et qualité amélioré après quelques semaines.
 
## Historique

2005 : Linus Torvalds initie le projet suite au besoin de changer le CVS (BitKeeper) pour le Kernel Linux

 * Design : distribué, sure, rapide et surtout _prendre CVS comme exemple de ce qu'il ne faut pas faire_ (ie. Subversion)
 * Démarré le 3 avril, annoncé le 6.
 * Le 16 juin, 1ere release du kernel avec GIT
 * le 26 juillet, le projet passe en maintenance et passe dans les main de Junio Hamano

## Caractéritiques principales
 
 * Complètement distribué
 * En ligne de commande !
 * Pas de deltas ("packfile") ce qui le différencie des autres DCVS
 * Support de gros projets
 * Fait pour le merge et la gestion des branches
 * Toolkit based design + protocols integration (ssh, tls, http, etc.)

## Bases

![local-remote](http://thkoch2001.github.com/whygitisbetter/images/local-remote.png)

http://ndpsoftware.com/git-cheatsheet.html

## Git Flavours

 * stash
 * bisect
 * cherry-pick
 * submodules

## Workflow 

###Subversion-Style Workflow
A very common Git workflow, especially from people transitioning from a centralized system, is a centralized workflow. Git will not allow you to push if someone has pushed since the last time you fetched, so a centralized model where all developers push to the same server works just fine.
subversion-style workflow

![svn-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-a.png)

###Integration Manager Workflow
Another common Git workflow is where there is an integration manager—a single person who commits to the 'blessed' repository, and then a number of developers who clone from that repository, push to their own independent repositories and ask the integrator to pull in their changes. This is the type of development model you often see with open source or GitHub repositories.
integration manager workflow

![itm-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-b.png)

###Dictator and Lieutenants Workflow
For more massive projects, you can setup your developers similar to the way the Linux kernel is run, where people are in charge of a specific subsystem of the project ('lieutenants') and merge in all changes that have to do with that subsystem. Then another integrator (the 'dictator') can pull changes from only his/her lieutenants and push those to the 'blessed' repository that everyone then clones from again.
dictator and lieutenants workflow

![oss-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-c.png)
