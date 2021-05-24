# SNCF, meeting 10-09-2020

- [ ] St Marcel il manque description de principes que Gregoire peut generer
- Rennes P23: la motie des proprietes n'a pas été testé
- [X] Automatisation n'est pas encore fini, ca devrai être rapide et pas trop difficile
- Fichiers AbstInfo: elle contient la spec generique pour une propriete donne
    - Ils utilisent des mots cles comme "signal source"
    - Ils contienent de variables que il faut garder de entre et soritie de systeme.
    - Le noms de principes que il faut instantier pour chaque element de specification. Ca donne fichier boxes pour chaque propriete.
- Il a fait passé 3.2 (il manque qulques encalchements)
- Il reste que les proprietes x_4
- Il a compris la difference enter 1.1 et 2.1
- SIEVE: un logiciel qui essaye de decouvrir les boites inutiles. Il a corrige
  des erreurs dans SIEVE.
  - Il en general retire 30% de boites pour le propriete 3.2. Mais le boites
    resultates ne sont pas suffisantes, car il y 2 chemins possibles pour
    montla propriete. Un chemin prenne 5 boites de plus et l'autre 3 boites de
    plus.
  - Le propriete ne passe pas en BDD, mais il est possible de decomposer le
    propriete à choses plus simples. 
- Proprietes longs: 1.2, 3.2
- [ ] Decouper les proprietes pour que BDD passe 1.2 3.2  
  - [ ] decoupage de 1.2 manuelement car il faut une grande mulinete pour ca 
  - il travaile sur decoupage 3.2. 
  - [ ] il faut implemener lancer SIEVE sur la liste complete de boites
- [ ] Documentation: 
  - description de proprietes: avancé mais pas encore presentable
