# Arqueo Bar — actualizaciones

Actualizaciones de la interfaz de la app Arqueo Bar. El celular las revisa e instala solo.

- `arqueo.json` — manifiesto firmado: `datos` (versión, notas, enlace al zip y su huella sha256)
  y `firma` (ECDSA P-256 / SHA-256 de `datos`, con la llave de Joseph).
- `arqueo-v<N>.zip` — la interfaz de la app.

La app solo instala lo que trae una firma válida de Joseph: cambiar estos archivos sin su llave
privada no tiene efecto en el celular. Los datos de la bartender nunca pasan por aquí.

Para publicar: `python -I herramientas/publicar.py --notas "Qué cambió"` desde la carpeta `arqueo-bar`.
