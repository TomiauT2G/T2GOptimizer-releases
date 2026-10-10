# T2G Optimizer · Releases

Aquí se publican las versiones de **T2G Optimizer**, el optimizador de Windows para jugar.
Este repositorio solo tiene los instaladores; el código fuente vive en otro lugar.

## Descargar

Ve a **Releases** y descarga la última versión:

- **Setup** (`T2G-Optimizer-Setup-x.y.z.exe`): instalador. La app se actualiza sola desde aquí.
- **Portable** (`T2G-Optimizer-Portable-x.y.z.exe`): no se instala. No se actualiza sola: la app
  avisa cuando hay una versión nueva y te lleva a esta página.

Requiere Windows 10 (1809 o posterior) u 11, de 64 bits, y permisos de administrador.

## Comprobar el archivo

Cada instalador trae su huella SHA-256 en la descripción de la versión. Para comprobarla:

```powershell
Get-FileHash .\T2G-Optimizer-Setup-x.y.z.exe -Algorithm SHA256
```

El resultado tiene que coincidir con la huella publicada. Los instaladores todavía no están
firmados con un certificado de código, así que SmartScreen puede mostrar un aviso.

## Archivos del canal de actualizaciones

Cada versión incluye `latest.yml` y su bloque de diferencias (`.blockmap`). Son los que lee la app
para saber qué versión hay y qué bajar. No hace falta descargarlos a mano.
