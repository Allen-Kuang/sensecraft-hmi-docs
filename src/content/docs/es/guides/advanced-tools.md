---
title: Herramientas avanzadas
description: Aprende a usar las herramientas de Flasher de firmware y Difuminado de imágenes para optimizar tu dispositivo y contenido para la mejor calidad de visualización.
---

## Introducción

La página de **Herramientas** en SenseCraft HMI proporciona un conjunto de utilidades avanzadas diseñadas para ayudarte a optimizar el contenido para tu pantalla y administrar el software de tu dispositivo. Esta sección está separada del espacio de trabajo de diseño principal y se centra en dos funciones clave:

1.  **Difuminado de imágenes**: Una herramienta poderosa para procesar y preparar imágenes para una calidad óptima en pantallas con paletas de colores limitadas, como las pantallas e-paper.
2.  **Flasher de firmware**: Una utilidad integrada para actualizar el firmware de tu dispositivo, asegurando que tenga las últimas características y correcciones de errores.

Esta guía te guiará a través de cada una de estas herramientas, explicando sus características y cómo usarlas de manera efectiva.

## Flasher de firmware

El Flasher de firmware es una herramienta esencial para mantener el software de tu dispositivo actualizado. Proporciona una interfaz simple, paso a paso, para flashear nuevo firmware directamente desde tu navegador web. Puedes instalar firmware oficial de SenseCraft HMI o firmware alternativo, como TRMNL, en dispositivos compatibles.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_46.png" style={{width:400, height:'auto'}}/></div>

### Firmware SenseCraft HMI vs TRMNL

Antes de flashear firmware, es importante entender las diferencias entre las dos opciones de firmware disponibles:

**Firmware SenseCraft HMI**
- Diseñado específicamente para la plataforma SenseCraft HMI
- Integración completa con las herramientas de diseño visual, plantillas y características de SenseCraft HMI
- Soporta diseño de UI personalizado a través del editor Canvas
- Acceso a las funciones de Generador de IA, feeds RSS, páginas Web y Galería
- Gestión de dispositivos en tiempo real a través del panel de SenseCraft HMI
- Recomendado para usuarios que desean una plataforma de diseño integral conectada a la nube

**Firmware TRMNL**
- Firmware alternativo de plataforma con su propio ecosistema
- Conjunto de interfaz y características diferente de SenseCraft HMI
- Gestionado a través de la plataforma y documentación de TRMNL
- No compatible con las características de la plataforma SenseCraft HMI

:::note
**Importante**: Si eliges flashear el firmware TRMNL, tu dispositivo ya no será compatible con la plataforma SenseCraft HMI. Deberás consultar la documentación oficial de TRMNL para obtener instrucciones de uso:

- **[TRMNL 7.5" (OG) DIY Kit con TRMNL](https://wiki.seeedstudio.com/ogdiy_kit_works_with_trmnl/)**
- **[Serie reTerminal E con TRMNL](https://wiki.seeedstudio.com/reterminal_e10xx_trmnl/)**

Para volver a SenseCraft HMI después de usar el firmware TRMNL, deberás volver a flashear el firmware de SenseCraft HMI usando la opción **Full Flash** para asegurar una instalación limpia.
:::

### Guía de flasheo paso a paso

#### Paso 1: Seleccionar tu dispositivo

Antes de comenzar, asegúrate de que tu dispositivo esté conectado a tu computadora a través de un cable USB.

1.  Haz clic en el botón **Seleccionar**.
2.  Aparecerá un modal pidiéndote que elijas tu dispositivo de una lista de hardware compatible.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_47.png" style={{width:400, height:'auto'}}/></div>

:::note
Si seleccionas el **ePaper DIY Kit - EE04**, se te solicitará un paso adicional: debes seleccionar el tipo y tamaño de pantalla específicos que estás usando con el kit. Esto asegura que los controladores de pantalla correctos estén incluidos en el firmware.
<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_48.png" style={{width:400, height:'auto'}}/></div>
:::

#### Paso 2: Seleccionar firmware

Una vez que se selecciona un dispositivo, las opciones de firmware estarán disponibles.

1.  Haz clic en el menú desplegable bajo **Seleccionar firmware** para ver una lista de versiones de firmware disponibles para tu dispositivo
2.  Elige el tipo y versión de firmware que deseas instalar:
    - **Firmware SenseCraft HMI** (Recomendado para usuarios de la plataforma SenseCraft HMI)
    - **Firmware TRMNL** (Plataforma alternativa - ver comparación arriba)

**Opciones adicionales:**
- **Conectar monitor serial**: Este botón abre un monitor serial en tu navegador, que es una herramienta avanzada para ver mensajes de depuración y registros del dispositivo durante el proceso de flasheo

#### Paso 3: Flash

Este es el paso final donde el firmware se escribe en el dispositivo.

1.  Haz clic en el botón **Flash** para comenzar el proceso. No desconectes el dispositivo ni cierres la pestaña del navegador hasta que esté completo.
2.  La herramienta mostrará una barra de progreso indicando el estado del flasheo.

:::tip
Verás una casilla de verificación etiquetada **Full Flash**. Ten mucho cuidado con esta opción.

**Flash estándar (sin marcar)**:
- Actualiza el firmware pero conserva tu configuración guardada en el almacenamiento no volátil del dispositivo, como tus credenciales de Wi-Fi
- Recomendado para actualizaciones regulares de firmware dentro de la misma plataforma

**Full Flash (marcado)**:
- Borra **toda** la memoria flash del dispositivo antes de escribir el nuevo firmware
- **Esto eliminará toda la configuración guardada, incluida tu contraseña de Wi-Fi**
- Necesitarás reconfigurar tu conexión Wi-Fi después de un Full Flash
- **Requerido al cambiar entre diferentes plataformas** (por ejemplo, de SenseCraft HMI a TRMNL, o viceversa)
- También se usa para solucionar problemas o realizar un "restablecimiento de fábrica"
:::

## Difuminado de imágenes

Las pantallas e-paper tienen características únicas y a menudo una paleta de colores limitada. La herramienta de Difuminado de imágenes procesa tus imágenes para que se vean mejor en estas pantallas mediante el uso de algoritmos especiales para simular tonos y colores. También se puede usar para generar archivos de encabezado de estilo C para desarrolladores que deseen incrustar imágenes directamente en su código.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_49.png" style={{width:400, height:'auto'}}/></div>

### Usar la herramienta de difuminado de imágenes

**Paso 1. Navegar y cargar**
*   Haz clic en **Herramientas** en la barra de navegación superior.
*   Asegúrate de que la pestaña **Difuminado de imágenes** esté seleccionada.
*   Haz clic en **Seleccionar imagen** para cargar una imagen desde tu computadora. También puedes hacer clic en **Editar imagen** para realizar ajustes básicos.

**Paso 2. Configurar las opciones de procesamiento**
Una vez que tu imagen esté cargada, usa el panel izquierdo para configurar cómo se procesará:

*   **Tipo de pantalla**: Selecciona el tipo de pantalla de destino (por ejemplo, `Black/White 1bpp`, `E6 Six-Color 4bpp`). Esto le dice a la herramienta cómo optimizar la imagen.
*   **Personalizado**: Establece manualmente la resolución de salida (Ancho y Alto) de la imagen. Esto generalmente debe coincidir con la resolución de pantalla de tu dispositivo.
*   **Algoritmo de difuminado**: Elige un algoritmo de difuminado. Diferentes algoritmos (como `Bayer 8x8`, `Floyd-Steinberg`) producen diferentes texturas visuales al simular colores. Experimenta para ver cuál se ve mejor para tu imagen.
*   **Invertir colores**: Alterna la imagen entre su estado de color normal e invertido.
*   **Corrección gamma**: Ajusta el brillo y el contraste de la imagen. Un valor más bajo generalmente hace que la imagen sea más oscura, mientras que un valor más alto la hace más brillante.
*   **ID de dispositivo**: Si planeas generar un archivo de encabezado, puedes establecer un ID personalizado aquí. Esto influirá en los nombres de variables (`Nombre de matriz`, `Macro de encabezado`) en el código generado.

**Paso 3. Vista previa y exportación**
Después de configurar las opciones, puedes elegir una de las siguientes acciones en la parte inferior:

*   **Vista previa**: Actualiza el área de visualización principal para mostrarte una vista previa en vivo de cómo se verá la imagen procesada final.
*   **Exportar imagen**: Descarga la imagen procesada a tu computadora como un archivo de imagen estándar (por ejemplo, PNG).
*   **Generar encabezado**: Para desarrolladores, esto crea y descarga un archivo de encabezado `.h` que contiene los datos de la imagen como una matriz de bytes, listo para ser incluido en un proyecto de firmware.

## Conclusión

La página de Herramientas ofrece utilidades indispensables tanto para diseñadores como para desarrolladores. Con la herramienta de Difuminado de imágenes, puedes asegurarte de que tus visuales estén perfectamente optimizados para tu pantalla, mientras que el Flasher de firmware proporciona una forma segura y fácil de administrar el software de tu dispositivo. Dominar estas herramientas te ayudará a aprovechar al máximo tu experiencia con SenseCraft HMI.

