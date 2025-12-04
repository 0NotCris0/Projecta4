# Servidor NFS

El primer que farem seran crear dos maquines virtuals, una sera el server NFS que sera un ubuntu i per ultim el client que sera un Zorin OS.

## Preparacio servidor 

Primer entrarem al servidor i actualizarem tot amb apt update && apt upgrade, i crearem dos grups que sera Devs i Admins. 

Lo seguent sera crear un usuari que es digui devs01 i que sigui membre del grup devs i un altre usuari que sera admin01 i de lgrup admins. 

## Creacio de directoris

Lo que farem sera crear un directori /srv/nfs/dev_projectes.  

```bash
cd /srv
mkdir nfs 
mkdir dev_projectes
```

