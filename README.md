# MyLittlePOS — Repositorio de artefactos

Repo **público y SOLO de distribución**: acá viven los instaladores y el manifiesto
`latest.json` que la app consulta desde **Acerca de → Buscar actualizaciones**.
No hay código fuente: el proyecto vive en `ramm-tec/mylittlepos-desktop` (Bitbucket).

La app está hardcodeada a este hosting:
`https://github.com/RicardoMunozXZ/mylittlepos-releases/raw/main/latest.json`
(constante `MANIFEST_URL` en `features/actualizaciones/data/ManifestActualizacionRepository.kt`).

## Flujo de publicación (una versión nueva)

1. Bump de `appVersion` en `gradle.properties` del repo de código (fuente única).
2. Compilar el instalador en Windows (el `.exe` sale de ahí).
3. En el repo de código, generar el manifest:
   ```bash
   ./scripts/release.sh dist/MyLittlePOS-<versión>.exe \
       "https://github.com/RicardoMunozXZ/mylittlepos-releases/raw/main/MyLittlePOS-<versión>.exe" \
       "Notas de la versión"
   ```
   El script calcula el sha256 y escribe `dist/latest.json`.
4. Copiar al repo espejo el instalador Y el `latest.json`, commitear y pushear a `main`:
   ```bash
   cp dist/MyLittlePOS-<versión>.exe dist/latest.json /ruta/al/espejo/
   cd /ruta/al/espejo
   git add . && git commit -m "release <versión>" && git push
   ```
5. Verificar: abrir la URL raw del `latest.json` en el navegador.

## Contrato de `latest.json`

```json
{
  "version": "1.1.0",
  "url": "https://github.com/RicardoMunozXZ/mylittlepos-releases/raw/main/MyLittlePOS-1.1.0.exe",
  "sha256": "<hash del instalador>",
  "notas": "Texto libre mostrado al usuario"
}
```

El `sha256` se verifica antes de lanzar el instalador: si no coincide, la descarga
se borra y la app informa el error. No publicar un manifest apuntando a un
instalador distinto al que se hash-eó.

**Atención con el crecimiento**: cada versión agrega su `.exe` al historial de git.
Si el repo crece demasiado, conviene mover los instaladores a GitHub *Releases*
(assets) y apuntar `url` ahí; `latest.json` puede quedarse en `raw/main`.
