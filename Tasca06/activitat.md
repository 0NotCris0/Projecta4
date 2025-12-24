# T06: Accés remot. Escriptori remot (RDP)

El primer que farem sera crear dues maquines virtuals una amb Windwos i l'altre amb Linux Zorin OS, la interficie de xarxa sera la per defecte NAT la segona sera host-only. Per pusarla en host-only haurem d'anar a la configuracio de xarxa en la maquinas virtuals i habilita una segona i posar nomes anfitrio.

img 1

Lo seguent sera entrar en la de windows i buscarem l'opció de Configuración de Escritorio Remoto.

img 2

I haurem d'acativar l'opcio de escritiorio remoto.

img 3

Ara ja podrem conectarnos i pasarem a la de Linux.

Haurem de configurar la maquina de Linux el Zorin OS, per asi aconseguir conectar-nos remotament a la de Windows.

Anirem a configuracio i despres a sharing, haurem d'activar la opcio de adalt.

img 4


Despres anirem a Remote desktop i activarem l'opcio de remote desktop i remote control, per poder controlar la maquina remotament. Per la contrasenya farem servir lo mateix usuari-usuari. 

img 5

Ara conectarem la maquina de windows a la de Zorin OS remotament hi ho farem amb Conexio a escritori remot.

img 6 

Posarem la IP del equip del Zorin OS, que sera aquesta: 

```bash
ip a
``` 

img 7

img 8

Posarem el nom d'usuari i la contrasenya que seran usuari-usuari com be hem dit abans.

img 9

Ens sortira una advertencia i li donarem que si.

img 10

I podem veure que ja estem a la maquina de Zorin remotament.

img 11

Ara lo seguent sera conectarme de Zorin a Windwos remotament.

Buscarem Remmina que esta per defecte en Zorin OS que sera la aplicacio que ens facilitara tot.

img 12

Mirarem la IP de la maquina de Windows amb ipconfig i sera aquesta:

img 13

Posarem la IP en Remmina.

img 14

Ens soritra una advertencia i li posem que Yes.

img 15

Ens demana el username i el password i les posem com abans. 

img 16

I ja podem veure la maquina de windows en Zorin.

img 17