---
title: "Des traceroutes plus court"
date: 2024-05-07T21:25:15+02:00
slug: 2024-05-07-traceroute
type: posts
draft: true
categories:
  - default
tags:
  - networking 
---

Dépanner des problèmes lié au routage ipv[46] a beau être une tâche passionnante, elle nous ramène souvent à cette bonne veille commande qu'est ``traceroute`` ou ``tracert`` sur Windows.

Les non-habitués seront étonné du temps de d'exécution de cette commande, elle peut être optimisé pour notre plus grand bien [^1].

>Pourquoi est-ce si long ?

Dans le cas de ``tracert`` la commande applique par défaut 
  - Une résolution DNS pour chaque routeur
  - Un délai d'expiration de chaque sonde (timeout) de 3 sec (long!!!)
  - Un TTL de maximum 30

En fonction des cas d'usage il convient de désactiver/abaisser pour réduire le temps d'éxécution 

Sur Windows :

```
tracert -w 500 -n 1.1.1.1
```

Sur les OS unix-like

```bash
traceroute -n 1.1.1.1
#
# démonstration
#
$ time traceroute 1.1.1.1 > /dev/null

real	0m1.291s
user	0m0.012s
sys	0m0.013s

$ time traceroute -n 1.1.1.1 > /dev/null

real	0m0.147s
user	0m0.002s
sys	0m0.015s
```




[^1]: post original sur [r/networking](https://www.reddit.com/r/networking/comments/1awfuqo/psa_your_traceroutes_are_slow_and_bad_and_they/)
