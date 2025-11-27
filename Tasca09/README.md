# Introducció

Molt bé, equip de consultors júniors.

En el nostre projecte ens trobem ara amb un requisit tècnic molt habitual per part dels nostres clients: **la centralització de dades en entorns Linux**.

---

# El Cas Client: *DevOptimize Solutions*

El nostre client, **DevOptimize Solutions**, és una petita startup de desenvolupament de programari que treballa exclusivament amb Linux. Actualment tenen un problema crític:

- El seu **codi font** i els seus **actius** (documents de disseny, scripts, recursos) estan **descontrolats**.  
- Cada desenvolupador treballa amb còpies locals disperses.  
- Això genera **conflictes de versions**, pèrdues d’hores de treball i un risc real de corrupció de dades.

Per aquest motiu, ens han contractat per implementar un **servidor de fitxers centralitzat** que permeti organitzar i unificar tot el flux de treball del seu equip.

Com que tot l’entorn és Linux, la solució nativa més ràpida, integrada i eficient és:

## 👉 **NFS (Network File System)**

---

# Requisits del Client

DevOptimize ha remarcat dues coses importants:

1. **Tot l’entorn és Linux**, tant servidors com estacions de treball.
2. **No disposen d’un sistema d’autenticació centralitzada** (LDAP, AD, FreeIPA…)  
   i **no tenen previst incorporar-lo de moment**.

Això implica que la gestió d’identitats (UID, GID) dependrà estrictament del servidor i dels clients, un punt crític que haurem de destacar a la demostració.

---

# La Teva Missió: Desenvolupar una Prova de Concepte (PoC)

Per mostrar al client com quedarà la solució i evidenciar tant les seves capacitats com les seves limitacions, has de preparar una demostració funcional completa.

## Hauràs de desplegar:

### 🖥️ **1. Un servidor NFS (NFSv3)**  
Que proporcioni directoris compartits mitjançant /etc/exports.

### 💻 **2. Un client Linux**  
Que consumeixi aquests recursos de manera persistent o sota demanda.

---

# Tasques que hauràs de realitzar

### 🔧 **Configuració del servidor NFS**
- Instal·lació del servei NFS.
- Configuració de directoris a compartir.
- Edició i aplicació de `/etc/exports` amb les opcions adequades.
- Explicació de les opcions clau d’exportació:
  - `rw`, `ro`
  - `sync`, `async`
  - `no_root_squash`, `root_squash`
  - restriccions per IP o subxarxa

---

### 👥 **Simulació de l'entorn del client**
Crea usuaris i grups per imitar diversos desenvolupadors:

- Creació d’usuaris (ex: *anna*, *marc*, *dev1*, *dev2*…).
- Assignació de grups (ex: *devteam*, *design*, etc.).
- Reproducció de la característica crítica dels entorns sense autenticació centralitzada:
  **Els UID/GID han de coincidir entre servidor i client.**

---

### 🔒 **Control d’accés**
Demonstra com combinar:

#### 1. **Permisos del sistema de fitxers**
- `chmod`
- `chown`
- `chgrp`

#### 2. **Opcions d’exportació de NFS**
per limitar:
- quin host accedeix,
- com hi accedeix,
- amb quin nivell de permisos.

Això permet mostrar clarament:

- Com es pot donar accés només al grup adequat.
- Com es pot impedir que un usuari o equip no autoritzat entri al recurs.
- Quines limitacions té NFSv3 en entorns sense LDAP.

---

# Objectiu final de la demostració

Quan la demo estigui preparada, el client ha de poder veure:

- El directori centralitzat visible des d’un client Linux.  
- Els permisos aplicats correctament.  
- Com els canvis aplicats al servidor afecten immediatament els clients.  
- On estan les limitacions de treballar sense autenticació centralitzada.

Aquesta PoC serà la base per validar el projecte i passar a la fase de desplegament real.

---

Si vols, puc continuar amb:

✅ Guia pas a pas per configurar el servidor NFS  
✅ Guia pas a pas per configurar el client  
✅ Exemple complet d’usuaris, permisos i proves  
✅ Explicació de les limitacions i recomanacions per al client  

- [Tornar pagina principal](../README.md)
- [Anar a la activitat](activitats.md)
