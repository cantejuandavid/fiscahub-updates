# fiscahub-updates

Publica **solo** `version.txt`: el sello de build de la ultima version de FiscaHUB.

FiscaHUB lo consulta al abrir, con una peticion HTTP asincrona, para avisar al auditor
si hay una version mas nueva. Es un archivo de una linea y no requiere autenticacion,
que es justo por lo que vive aqui y no en OneDrive.

**El codigo NO se publica en este repositorio.** La actualizacion del modulo se hace
desde la carpeta compartida de OneDrive (`FiscaHUB_Update.xlsx`), que exige cuenta de
la organizacion.

## Publicar un build

`_gen_update_xlsx.py` escribe aqui el `version.txt` en cada build. Solo queda:

    git commit -am "bNNN" && git push
