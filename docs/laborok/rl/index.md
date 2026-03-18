# RL Labor

## A labor célja

Ennek a laboranyagnak **nem az a célja**, hogy teljesen nulláról, önállóan találd ki, hogyan kell a különböző reinforcement learning algoritmusokat implementálni és használni.

A notebookokat azért állítottam össze, hogy a **már létező, működő megoldásokon keresztül** értsd meg:

- hogyan működik egy RL-környezet a gyakorlatban,
- hogyan viselkednek a különböző algoritmusok,
- milyen szerepe van az egyes hiperparamétereknek,
- és hogyan befolyásolják ezek a tanulás stabilitását, sebességét és eredményességét.

Ez a labor tehát elsősorban **értelmező és kísérletező szemléletű**.  
A hangsúly azon van, hogy:

- futtass meglévő megoldásokat,
- figyeld meg a tanulási görbéket és a policy viselkedését,
- próbáld ki különböző beállításokat,
- és ezek alapján értsd meg az algoritmusok közötti különbségeket.

## A labor felépítése

A labort több notebookból építettem fel, amelyek egymásra épülnek:

1. **RL környezetek alapjai és vizualizáció**
2. **Q-learning**
3. **DQN**
4. **PPO**
5. **Projektfeladat felvezetése**

A notebookokban kész vagy majdnem kész megoldásokat adok, és ezek alapján azt kérem tőled, hogy:

- értsd meg a fontos lépéseket,
- értelmezd az ábrákat és animációkat,
- válaszold meg a notebookok végén található kérdéseket,
- majd a megszerzett tapasztalatokat alkalmazd egy saját projektben.

## Mit várok el a notebookok használata során?

A notebookokkal való munka során nemcsak azt várom tőled, hogy lefuttasd a cellákat, hanem azt is, hogy tudatosan figyeld meg például:

- hogyan változik a tanulás különböző hiperparaméterek mellett,
- mikor stabil vagy instabil egy algoritmus,
- hogyan viselkedik az exploráció,
- milyen különbség látszik a tanulatlan és a betanított policy között,
- és milyen környezetekhez milyen algoritmus illik jobban.

## A beadandó

!!! warning 
    A laborhoz a **megoldas.ipynb notebookot** kérem beadni. Ebben a notebookban neked egy saját magad által kiválasztott környezeten kell bemutatnod legalább egy, a labor során megismert algoritmus alkalmazását.

### A beadandó alapfeladata

1. választasz egy környezetet,
2. röviden bemutatod azt,
3. kiválasztasz egy megfelelő algoritmust,
4. betanítasz egy modellt,
5. kiértékeled annak teljesítményét,
6. és röviden értelmezed az eredményeket.

### Fontos megjegyzés a beadandóhoz

A beadandóval **nem** az a célom, hogy a lehető legnehezebb környezetet válaszd, és nem is az, hogy minden esetben tökéletes eredményt érj el.

Nálam ezek a fő szempontok:

- jó környezetválasztás,
- indokolt algoritmusválasztás,
- átlátható kísérletezés,
- helyes értelmezés,
- és a tanulási folyamat megértése.

Vagyis egy egyszerűbb, de jól bemutatott és jól értelmezett projekt nálam értékesebb lehet, mint egy túl nehéz, de átgondolatlan választás.

### Megajánlott jegyhez

!!! example "Opcionális feladat beadandó (10 pont)"
    * Két környezet feldolgozása két külön algoritmussal
    * Mindkét megoldás részletes leírása