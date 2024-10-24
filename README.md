# FCSC 2023 SPAnosaurus

La société MegaSecure vient d'éditer une mise à jour de sécurité pour leurs serveurs. 
Après analyse de la mise à jour, vous vous apercevez que l'éditeur utilise maintenant 
ce code pour l'exponentiation :

```c
unsigned long exp_by_squaring(unsigned long x, unsigned long n) {
  // n est l'exposant secret
  if (n == 0) {
    return 1;
  } else if (n % 2 == 0) {
    return exp_by_squaring(x * x, n / 2);
  } else {
    return x * exp_by_squaring(x * x, (n - 1) / 2);
  }
}
```

Vous avez accès à un serveur où vous avez pu lancer en tant qu'utilisateur ```exp_by_squaring(2, 2727955623)```
tout en mesurant sa consommation d'énergie. L'exposant ici est donc ```n = 2727955623```, soit ```10100010100110010100110010100111``` 
en binaire. Cette trace de consommation est sauvegardée dans ```trace_utilisateur.csv```.

Vous avez également réussi à mesurer la consommation d'énergie pendant l'exponentiation d'une donnée de l'administrateur. 
Cette trace de consommation est sauvegardée dans ```trace_admin.csv```. Saurez-vous retrouver son exposant secret n ?

Le flag est au format ```FCSC{1234567890}``` avec ```1234567890``` à remplacer par l'exposant secret de l'administrateur écrit en décimal.

![spanosaurus.png](spanosaurus.png)


Fichiers :
- [trace_utilisateur.csv](trace_utilisateur.csv) 
- [trace_admin.csv](trace_admin.csv)


Auteur : erdnaxe

Origine : [SPAnosaurus](https://hackropole.fr/fr/challenges/hardware/fcsc2023-hardware-spanosaurus/)


-----------

## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2023-hardware-spanosaurus.git

> cd fcsc2023-hardware-spanosaurus


-----------

## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/hardware/fcsc2023-hardware-spanosaurus/