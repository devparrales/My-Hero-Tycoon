# 02_model_del_joc.md

## 1. Components principals del joc

El joc *My Hero Tycoon* és un mini-tycoon desenvolupat en Roblox basat en la generació i gestió de diners mitjançant un sistema de millores.

Els components principals del joc són:

- Sistema de diners (economia del jugador)
- Sistema de droppers (generació automàtica)
- Sistema de compra (botons)
- Sistema de recollida (collector)
- Base del jugador (tycoon)

Aquests components formen el bucle principal del joc: generar diners → recollir-los → invertir-los en millores.

---

## 2. Entitats identificades

Les entitats principals del sistema són:

- **Player (Jugador)**
- **Tycoon (Base del jugador)**
- **Dropper**
- **Button (Botó de compra)**
- **MoneyCollector**

Aquestes entitats representen tots els elements necessaris per implementar la lògica del joc.

---

## 3. Atributs clau de cada entitat

### Player
- `money`: quantitat de diners del jugador
- `tycoon`: referència a la seva base

### Tycoon
- `owner`: jugador propietari
- `droppers`: llista de droppers disponibles
- `buttons`: llista de botons de compra
- `collector`: sistema de recollida de diners

### Dropper
- `value`: diners generats per cicle
- `speed`: freqüència de generació
- `active`: indica si està actiu

### Button
- `price`: cost de la millora
- `itemUnlocked`: element que desbloqueja
- `purchased`: estat de compra

### MoneyCollector
- `storedMoney`: diners acumulats
- `multiplier`: multiplicador de guanys

---

## 4. Accions, mètodes o funcions principals

### Player
- `addMoney(amount)`: afegeix diners
- `spendMoney(amount)`: resta diners

### Tycoon
- `assignOwner(player)`: assigna propietari
- `addDropper(dropper)`: afegeix un dropper
- `unlockItem(item)`: desbloqueja una millora

### Dropper
- `generateMoney()`: genera diners automàticament
- `activate()`: activa el dropper

### Button
- `onTouch(player)`: detecta interacció
- `purchase(player)`: gestiona la compra

### MoneyCollector
- `addMoney(amount)`: guarda diners
- `collect(player)`: dona els diners al jugador

---

## 5. Explicació del diagrama de classes

El diagrama de classes representa l’estructura del sistema i les relacions entre entitats.

- El **Player** té associat un **Tycoon**
- El **Tycoon** conté els elements del joc (Dropper, Button i MoneyCollector)
- Els **Dropper** generen diners que s’envien al **MoneyCollector**
- Els **Button** permeten desbloquejar millores dins del Tycoon

Aquest model està organitzat per responsabilitats:
- El Player gestiona diners
- El Tycoon organitza els components
- Els Dropper generen recursos
- Els Button controlen el progrés del joc

Aquesta separació facilita una implementació clara en scripts dins de Roblox.

---

## 6. Explicació del diagrama de comportament

S’ha utilitzat un **diagrama d’activitat** per representar el flux del joc.

El procés és el següent:

1. Els droppers generen diners de forma automàtica
2. Els diners es guarden al collector
3. El jugador recull els diners
4. El jugador decideix si compra una millora
5. Si compra, es desbloquegen nous elements
6. Augmenta la producció
7. El bucle es repeteix

Aquest diagrama reflecteix el bucle principal del joc, que és la base de qualsevol tycoon.

---

## 7. Correspondència entre diagrames i codi futur

Els diagrames es traduiran directament a l’estructura del codi en Roblox Studio:

- **Player** → sistema de `leaderstats` (diners)
- **Tycoon** → Model dins del Workspace
- **Dropper** → Part amb Script que genera diners (loop amb `task.wait()`)
- **Button** → Part amb esdeveniment `.Touched`
- **MoneyCollector** → Part amb detecció de contacte

Exemples:
- `generateMoney()` → bucle que crea diners periòdicament
- `onTouch()` → funció activada quan el jugador toca el botó
- `collect()` → transferència de diners al jugador

Aquesta correspondència assegura que el model no és teòric, sinó directament aplicable.

---

## 8. Estructura inicial del repositori

L’estructura del projecte serà:
MyHeroTycoon/
│
├── README.md
├── src/
│ ├── player/
│ │ └── money.lua
│ ├── tycoon/
│ │ ├── tycoon.lua
│ │ ├── dropper.lua
│ │ ├── button.lua
│ │ └── collector.lua
│
├── assets/
│ └── models/
│
├── diagrames/
│ ├── diagrama_classes.png
│ └── diagrama_comportament.png

Aquesta estructura permet separar la lògica per responsabilitats i facilita el manteniment del codi.

---

## 9. Primer commit i README inicial

### Primer commit

Missatge del commit:
`Initial commit - estructura base del projecte My Hero Tycoon`

Contingut:
- Fitxer README.md
- Carpetes del projecte
- Carpeta de diagrames (amb o sense imatges inicials)

Aquest commit serveix com a punt d’inici del desenvolupament.

---

### README inicial

El README inclourà:

- Nom del projecte: **My Hero Tycoon**
- Descripció breu del joc
- Objectiu del jugador
- Tecnologies utilitzades (Roblox Studio i Lua)
- Autor del projecte

Exemple:

# My Hero Tycoon

Mini-tycoon de superherois desenvolupat amb Roblox Studio.

L’objectiu del joc és generar diners i millorar la base del jugador mitjançant droppers i millores.

Tecnologies:
- Roblox Studio
- Lua

Autor: Joan Parra Catherine