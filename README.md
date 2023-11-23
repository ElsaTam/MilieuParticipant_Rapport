Ce rapport, réalisé durant un stage de deux mois, est découpé en deux grandes parties.

La première (chapitres 1 à 5) contient un résumé des principes mathématiques et informatiques du transfert de lumière au sein d'un milieu participant. La théorie y est abordée, couvrant :
- l'équation de transport de la lumière (LTE) de l'émetteur vers le récepteur (dite *équation de rendu*) ainsi que du récepteur vers l'émetteur (dite *équation en potentiel*);
- les fonctions de phase, analogues volumétriques des BSDFs, telles que celle de Henyey-Greenstein, de Schlick, de Rayleigh, ou encore de Mie;
- les types d'interaction entre la lumière et le milieu participant qu'elle traverse (l'absorption et l'*out-scattering* pour l'extinction, et l'émission et l'*in-scattering* pour la source);
- l'équation de transfert, équivalent de la LTE mais prenant en compte les interactions avec le milieu participant.

Les techniques informatiques pour passer des intégrations continues à des calculs discrets sur ordinateur sont également décrites (simulation de Monte Carlo, échantillonnage d'importance, etc.) ainsi que la méthode d'optimisation par *Next Event Estimation* (NEE).

La deuxième partie (chapitres 6 à 10) présentent des algorithmes mis en place et explorés (chapitres 6, 7, 8) durant mon stage, avec pour objectif de prendre en compte le temps que la lumière met pour aller de l'émetteur au récepteur (ou inversement) par différents chemins. Durant son transfert dans la fumée, la lumière ne se déplace pas en ligne droite et peut, en tout point du chemin, avoir une probabilité non nulle d'être dispersée vers l'émetteur. De fait, le signal lumineux arrive de manière déconstruite à l'émetteur. L'objectif de ces travaux est de proposer une piste de départ pour simuler un signal reçu sur toute une durée, et de reconstruire le signal envoyé à un instant $t$.