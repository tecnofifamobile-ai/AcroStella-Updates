# AcroStella Analytics

Instaladores Android y paquetes iOS para firma. El código fuente y los vídeos permanecen privados.

- **Android:** [APK 0.7.0 · build 9](https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/refs/tags/v0.7.0%2B9/acrostella-analytics-0.7.0%2B9.apk), también en la [última versión estable](https://github.com/tecnofifamobile-ai/AcroStella-Updates/releases/latest).
- **iPad/iPhone:** [IPA 0.6.0 sin firma](https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/refs/tags/ios-v0.6.0%2B8/acrostella-analytics-0.6.0%2B8-unsigned.ipa). Importar y firmar en Flarestore con el certificado/perfil del usuario, conservando el identificador de su instalación. Las versiones iOS son prereleases para mantener separado el canal Android.

## Android 0.7.0 — AcroStella Hub

Dashboard con Analytics, Workspace, Dispositivos, Archivos y Ajustes. Conserva la grabación al navegar y el estado de revisión, importa documentos privados y mantiene las cámaras/anotaciones. Misma firma Android para actualizar. La integración GameStream nativa es inicialmente iPadOS; no se presenta como motor remoto Android.

El canal público iOS permanece en 0.6.0. No se anuncia una IPA 0.7.0 hasta preparar su distribución completa. Los vídeos y certificados del usuario no se publican.

## Actualizar dentro de AcroStella

**Actualizaciones → Buscar actualizaciones** descarga el paquete desde GitHub y verifica tamaño y SHA-256. Android vuelve a comprobar identidad y firmante antes de abrir el instalador del sistema. En iPad, **Enviar IPA al firmador** abre la hoja de compartir; también se puede guardar en Archivos e importar en Flarestore. Allí se firma e instala. Compartir no significa que se haya instalado: la app consulta la versión al regresar.

No desinstalar para actualizar: borrar la aplicación puede eliminar su biblioteca. La IPA sin firma no se instala directamente desde Safari. No se publican certificados ni se firma iOS en el servidor.

## Fuentes para Flarestore

Fuente principal, formato AltStore:

```text
https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/main/flarestore.json
```

Fuente de compatibilidad ya existente:

```text
https://raw.githubusercontent.com/tecnofifamobile-ai/AcroStella-Updates/main/flarestore-latest.json
```

Ambas ofrecen únicamente 0.6.0, build 8, y mantienen sus identidades y direcciones para futuras publicaciones. No hace falta crear una fuente nueva en cada versión. Si el catálogo del firmador conserva una versión antigua, AcroStella consulta GitHub directamente desde Actualizaciones; se puede importar manualmente la IPA del enlace anterior. Los paquetes antiguos siguen disponibles en sus Releases.

## Dos cámaras, conexión recordada y revisión conjunta

Usar 0.6.0 o posterior en ambos dispositivos: el protocolo de cámaras v3 se conserva en Android 0.7.0; las versiones anteriores a 0.6.0 no son compatibles. Conectar el iPad y el Android a la misma Wi-Fi o al hotspot del Android y autorizar cámara/red local. En Android: **Dispositivos → Usar como segunda cámara**. En el iPad: **Buscar cámaras → tocar la cámara → Conectar y recordar** con las seis cifras. Después se recuerda la confianza y se reconecta al regresar a la app; la conexión manual por IP sigue disponible si no funciona el descubrimiento.

El iPad muestra ambas cámaras en directo a partes iguales. **Iniciar · dos ángulos → Revisar** coordina los archivos y reúne el segundo original para revisión/guardado comunes. Los vídeos terminados, su correlación de tiempos y los acuses pendientes se conservan para recuperarlos tras cortes. La copia del Android permanece hasta eliminarla desde su biblioteca.

El directo tiene latencia; la revisión usa los originales y la alineación inicial del primer frame aceptado por el grabador nativo, con ajuste visual manual. Comprobar una palmada o movimiento común: cero desfase físico no está garantizado. El sistema puede suspender la cámara al abandonar o bloquear la app; se conserva la confianza, pero no se graba en segundo plano. No hay todavía búfer circular/replay comprimido continuo.

Estudio adaptado a móvil/tablet y Liquid Glass nativo en iOS 26+; material alternativo en sistemas anteriores y renderer Flutter en Android compatible. La pantalla evita apagarse con cámara activa en primer plano. Sin cuentas, nube ni body tracking. Los vídeos no se suben a GitHub.

La compilación y las pruebas con cámaras sintéticas no sustituyen validar directo, orientación, hotspot, calor y alineación en el iPad y el Android. La instalación de esta versión debe comprobarse en el dispositivo.
