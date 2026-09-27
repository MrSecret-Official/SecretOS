# SecretOS

Imágenes ISO de SecretOS, firmadas. Aquí no hay código: solo las versiones publicadas (sección **Releases**).

## Descargar

GitHub no admite archivos de más de 2 GB, así que la ISO va en partes (`secretos.iso.part01`, `part02`...). Descarga todas las de la última versión y únelas:

- Windows (cmd): `copy /b secretos.iso.part01 + secretos.iso.part02 + secretos.iso.part03 + secretos.iso.part04 secretos.iso` (pon todas las partes, en orden)
- Linux o macOS: `cat secretos.iso.part* > secretos.iso`

Comprueba el resultado con `secretos.iso.sha256` (Linux: `sha256sum -c secretos.iso.sha256`; Windows: `Get-FileHash secretos.iso`).

## Verificación

`secretos.iso.manifest` enumera la ISO y cada parte con su tamaño y su suma SHA-256. Los archivos `.sig` son firmas Ed25519 de SecretOS. Los equipos con SecretOS descargan y comprueban todo esto solos: sin una firma válida no aceptan nada.
