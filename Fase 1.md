# 01_idea_i_abast.md

## 1. Títol provisional del joc
**My Hero Tycoon**

## 2. Tipus de microvideojoc escollit
Mini-tycoon en Roblox (gestió simple amb droppers i upgrades).

## 3. Objectiu del joc
Construir una base de superheroi i generar diners automàticament per millorar-la.

## 4. Rol del jugador
El jugador controla un personatge dins Roblox que pot:

- Caminar per la base
- Comprar millores tocant botons (pads)
- Recollir diners generats

## 5. Regles bàsiques
- El jugador comença amb una base buida.
- Pot comprar un “dropper” inicial.
- Els droppers generen diners amb el temps.
- Els diners es recullen en un collector.
- Amb diners es poden desbloquejar millores.

## 6. Condicions de victòria i derrota
**Victòria:**
- Comprar totes les millores disponibles (tycoon complet).

**Derrota:**
- No hi ha derrota.

## 7. Bucle principal del joc
1. Generar diners (droppers).
2. Recollir diners.
3. Comprar millores.
4. Augmentar producció.
5. Repetir.

## 8. Repte principal i dificultat
**Repte:**
Optimitzar la compra de millores.

**Dificultat:**
- Baixa (progressiva i accessible).

## 9. Limitacions explícites
El joc NO inclourà:
- Combat entre jugadors
- Poder usar habilitats d’heroi
- Multijugador competitiu complex
- Múltiples tycoons diferents
- Sistema de guardat (DataStore)
- Animacions avançades
- UI complexa

## 10. Riscos tècnics
1. Scripts de droppers (generació contínua d’objectes).
2. Sistema de compra (detectar toc del jugador).
3. Errors amb col·lisions o recollida de diners.

## 11. Exploració amb IA

### Prompt 1
"How to make a simple tycoon in Roblox Studio step by step"

**Resposta resumida:**
- Crear base
- Afegir droppers
- Afegir collector
- Scripts en Lua per generar diners

### Prompt 2
"Roblox Lua script for button purchase system tycoon"

**Resposta resumida:**
- Detectar Touch amb .Touched
- Comprovar diners del jugador
- Restar diners
- Activar objecte

## 12. Proposta final escollida
Mini-tycoon de superheroi amb:
- 1 base
- 2-3 droppers
- 3-5 millores

## 13. Justificació de viabilitat
- Roblox ja té física i moviment fets.
- No cal crear motor des de zero.
- Sistema simple de scripts en Lua.
- Nombre limitat d’elements → viable en 10 hores.

## 14. Mini pla de treball

**Fase 1 (1.5h):**
Documentació.

**Fase 2 (2h):**
Crear base i mapa.

**Fase 3 (3h):**
Droppers + generació de diners.

**Fase 4 (2h):**
Sistema de compra (botons).

**Fase 5 (1.5h):**
Test i correcció.

## 15. Eines previstes i justificació

- **Roblox Studio** → creació del joc i scripts.
- **Lua** → programació.
- **Toolbox (Roblox)** → assets bàsics (opcionales).

Justificació:
Roblox permet crear jocs ràpidament amb scripts simples i assets ja disponibles, ideal per un projecte curt.