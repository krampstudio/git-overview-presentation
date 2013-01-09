git-overview-presentation
=========================

French overview/presentation of GIT

#Git Développez Autrement !

![git](http://git-scm.com/images/logos/1color-lightbg@2x.png)

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

Interactive cheat sheet: http://ndpsoftware.com/git-cheatsheet.html

### Branches

![branches-sample]imgs/github_branches.png)

Types de branches:
 
 * Local / Remote
   * local tracking remote
 * Orphelines ou non (attention!) 

Utilisation de branches:

 * Topic branches
 * Long term branches
 * Worflow based branches

Stategies de merge: 

 * merging
 * rebasing

## Git Flavours

> small demo for each ones

 * stash
 * bisect
 * cherry-pick
 * submodules

## Workflow 

###Subversion-Style Workflow
Un dépots distant qui centralise les dépôts locaux. 
(attention aux merges!)

![svn-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-a.png)

###Integration Manager Workflow
Une seule personne (l'intégration manager) fait les merges et commit vers le _blessed repository_

![itm-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-b.png)

###Dictator and Lieutenants Workflow
Modèle à la _linux kernel_. Pour les gros projets

![oss-wrokflow](http://thkoch2001.github.com/whygitisbetter/images/workflow-c.png)

###Do what you fuck you want!

## Tools
 
### Base GIT

 * CLI (GIT bash for windows)
 * TortoiseGit (W$)
 * SourceTree (OSX)
 * Giggle
 * Gitk
 * etc.

### Integration

 * Supporté dans les IDEs
 * git-svn, git-cvs, git-hg
