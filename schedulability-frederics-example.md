# Schedulability: Frederics example

Frederic writes:
Nous avons travaillé sur le papier avec Sarah. Par chance, nous avons trouvé un document plus long et des modèles qui nous ont permis de comprendre certains aspects très obscurs dans le papier: https://sw10.lmz.dk/ (section 7.2.5 du rapport). Nous l’avons adapté pour pouvoir le traiter avec nos outils. J’aimerais ton avis sur ce modèle en PJ.

Le modèle de l'article a 3 caractéristiques importantes:
- il utilise des stopwatches pour modéliser la préemption d’une tâche moins prioritaire par une tâche plus prioritaire.
- il réduit “schedulable” à “no deadlock”
- il a relativement peu de concurrence. Les seules actions concurrentes sont celles constituants la séquence de trois états committed (C) en Figure 2. Un thread peut exécuter cette séquence en même qu’un autre thread exécute la même sequence, ou alors qu’un autre thread attend dans l’état CheckForOffset, ou enfin, alors qu’un autre thread est dans l’état ExecutingThread ou dans l’état Done. Mais du fait de la priorité donnée aux threads qui sont dans des états committed, les deux dernières situations ne donnent aucune concurrence. Le thread dans l’état committed exécutera ses deux transitions menant à ReadyToBeScheduled alors qu’un thread dans CheckForOffset ou dans ExecutingThread ou dans DONE ne fera aucune action. In fine, la seule situation de réelle concurrence est celle de threads situés dans l’une des 3 locations committed. Ces threads ayant la même priorité (tous committed), tous les entrelacements d’actions peuvent se produire.

Nous avons donc fait plusieurs choix:
- pas de préemption: cela permet d’éviter les stopwatches. Cela ne réduit pas la concurrence dans le modèle puisque la seule situation de vraie concurrence (voir ci-dessus) est préservée. Les situations de preemption sont supprimées, mais comme indiqué ci-dessus, il n’y a pas de réelle concurrence dans ce cas.
- réduction de “schedulable” à “safety”. Nous n’avons pas d’algorithme de détection de deadlock, donc pas le choix.
- nous n’avons pas modélisé le code des threads (Figure 5 de l’article) pour le moment afin de simplifier le modèle. Mais, on peut l’ajouter très facilement.

Tu trouveras notre modèle UPPAAL en PJ. Ce modèle a des variables partagées, nous écrirons un modèle client/serveur et/ou global/local ensuite. J’aimerais ton avis sur ce modèle. Plus précisément: 
- notre modèle utilise une variable partagée “schedulable” qui permet au thread T d’indiquer s’il est prêt à s’exécuter (schedulable[T] := true) ou non (schedulable[T] := false). Dans une version client/serveur ou global/local du modèle, ces variables seront gérées par le Scheduler (qui joue le rôle du serveur). Les threads mettront à jour les variables via des communications. Du coup, la concurrence va se réduire très fortement. Il ne restera plus que la séquence CheckForOffset -> Release -> Schedulable (1 action locale suivie de 1 communication) où nous pouvons espérer un gain (modeste).
- une solution pour gagner en concurrence serait de considérer qu’on dispose de plusieurs cœurs de calcul. On peut donc exécuter plusieurs threads en parallèle. En ajoutant le code des threads comme en Figure 5 de l’article, on va fortement gagner avec nos techniques client/serveur ou global/local. En effet, le code des threads est constitué essentiellement d’actions locales. Nos algorithmes vont éviter les entrelacements des actions des différents threads, contrairement à l’algorithme standard d’accessibilité.

Voilà donc où nous en sommes. Je souhaite savoir si c’est conforme à ce que tu imaginais d’après cet article, et si passer le modèle en “multicore scheduling” te semble être une bonne idée.


#partial-order
#real-time
