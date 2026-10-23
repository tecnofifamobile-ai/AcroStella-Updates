# AcroStella Analytics

Instaladores Android y paquetes iOS para firma. El código fuente y los vídeos permanecen privados.

- **Android:** descarga el APK en la [última versión estable](https://github.com/tecnofifamobile-ai/AcroStella-Updates/releases/latest). Desde 0.3.0 las actualizaciones se ofrecen dentro de la app.
- **iPad/iPhone:** [IPA 0.5.2 sin firma](https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/refs/tags/ios-v0.5.2%2B7/acrostella-analytics-0.5.2%2B7-unsigned.ipa). Importar en Flarestore y firmar con certificado/perfil válidos antes de instalar. Las versiones iOS figuran como prereleases para mantener separado el canal Android.

La IPA sin firma no se instala directamente desde Safari. Certificado, perfil y funcionamiento físico requieren validación en el dispositivo.

## Fuente para Flarestore

Añade esta URL como source (formato AltStore):

```text
https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/main/flarestore.json
```

La fuente ofrece la IPA sin firma. Descárgala desde Flarestore y fírmala con tu certificado y perfil antes de instalar. El usuario ha confirmado la instalación de 0.4.0 en iOS. La versión 0.5.2 y el flujo con dos cámaras necesitan su propia prueba física. La URL de la fuente se mantiene para futuras versiones; cada IPA apunta a una etiqueta fija.

## Actualizar en el iPad desde AcroStella

En la versión actual, abre **Actualizaciones → Buscar actualizaciones** en AcroStella. Consulta GitHub directamente y descarga la IPA con comprobación de tamaño y SHA-256, sin depender del aviso del catálogo de Flarestore. **Enviar IPA al firmador** abre la hoja de compartir: escoger un firmador compatible o guardar en Archivos e importar en Flarestore. Allí se firma e instala conservando el identificador anterior.

Para estrenar este método, importa una vez la IPA actual del enlace anterior. Compartir la IPA no confirma su instalación; la versión instalada se comprueba al volver. Las fuentes siguen disponibles y conservan sus identidades. No hace falta crear otra fuente en cada versión.

## Dos ángulos en 0.5.2

Actualizar ambos dispositivos. Conectarlos a la misma Wi-Fi o al hotspot del Android. En Android: Dispositivos → Usar como segunda cámara. En el iPad: pulsar Buscar cámaras, elegir el Android e introducir sus seis cifras; si no aparece, usar Conexión manual por IP; autorizar red local y cámara. Iniciar y terminar desde el iPad, esperar la transferencia y revisar/guardar ambos ángulos juntos. Mantener ambas apps abiertas y las pantallas desbloqueadas.

La transferencia de vídeo está cifrada y se comprueba antes de adjuntar el archivo. Los vídeos no se suben a GitHub ni a una nube. Comprobar una palmada o movimiento común y corregir la alineación si hace falta; cero desfase físico no está garantizado. Esta entrega transfiere al finalizar y no ofrece vista remota en directo ni captura continua. La copia del Android se conserva hasta eliminarla desde su biblioteca.

## Si Flarestore sigue mostrando 0.4.0

La fuente principal contiene únicamente la versión actual para evitar selecciones de una entrada antigua del historial. Si el cliente conserva 0.4.0, elimina únicamente la fuente anterior de su lista de Fuentes y añade esta URL de compatibilidad, con identidad y dirección nuevas:

```text
https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/main/flarestore-latest.json
```

Debe ofrecer 0.5.2, build 7. No desinstales AcroStella; descarga y firma manteniendo el identificador de la instalación anterior. Las IPA antiguas siguen disponibles en sus Releases. En futuras publicaciones se actualizan `flarestore.json` y `flarestore-latest.json` a la misma versión actual, manteniendo sus identidades y direcciones propias.
