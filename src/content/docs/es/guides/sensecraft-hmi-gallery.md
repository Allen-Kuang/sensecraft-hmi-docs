---
title: Función de galería
description: Presenta el uso de Galería, una función de la plataforma SenseCraft HMI.
---

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/66.jpg" style={{width:800, height:'auto'}}/></div>

## Introducción

La función de Galería en [SenseCraft HMI](https://sensecraft.seeed.cc/hmi) te permite transformar tus dispositivos con pantalla en hermosos marcos de fotos digitales. Puedes cargar imágenes locales o importarlas desde URLs, y luego mostrarlas con intervalos de transición personalizables y efectos visuales. Esta función es perfecta para crear pantallas ambientales, pantallas de información o álbumes de fotos decorativos usando tus dispositivos de pantalla Seeed Studio.

Este tutorial te guiará en el uso de la función de Galería en SenseCraft HMI, cubriendo métodos de carga de imágenes, configuración de visualización y consideraciones importantes para un rendimiento óptimo.

Este artículo utilizará el [reTerminal E1002](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/) como ejemplo para explicar cómo usar esta función en la plataforma SenseCraft HMI.

## Primeros pasos con Galería

### Acceder a la función de Galería

**Paso 1.** Navega a la plataforma SenseCraft HMI a continuación.<br/>

[SenseCraft HMI](https://sensecraft.seeed.cc/hmi)<br/>

**Paso 2.** Conecta tu dispositivo o selecciona un dispositivo ya emparejado para usar.<br/>
**Paso 3.** Haz clic en **Galería de imágenes** y puedes elegir cargar imágenes locales o importar imágenes desde una URL.<br/>

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_start_1.png" style={{width:800, height:'auto'}}/></div>

### Comprender la interfaz de Galería

La interfaz de Galería consta de varios elementos clave:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_interface_1.png" style={{width:800, height:'auto'}}/></div>

1. **Panel de control**: Esta sección incluye la configuración para agregar los elementos añadidos, Listas de páginas, modos de difuminado y la dirección de visualización de las imágenes.
2. **Área de visualización de imagen**: La sección principal donde se muestra tu imagen actual
3. **Barra de herramientas de imagen**: Contiene herramientas para ajustar o descargar la imagen actual
4. **Tira de miniaturas**: Muestra todas las imágenes cargadas en tu galería
5. **Botones de acción**: Botones de Guardar, Vista previa e Implementar para probar y aplicar tu galería al dispositivo

## Agregar imágenes a tu galería

SenseCraft HMI proporciona dos métodos para agregar imágenes a tu galería: cargar archivos locales o importar desde URLs.

### Cargar imágenes locales

Paso 1. Haz clic en el botón **Nuevo** en el panel de control

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_img_1.png" style={{width:800, height:'auto'}}/></div>

**Paso 2.** En el cuadro de diálogo que aparece, selecciona **Galería de imágenes**, y en el cuadro de diálogo emergente, haz tu selección.**Cargar archivo**<br>
**Paso 3.** Haz clic en **Seleccionar archivos de imagen**, y elige las imágenes que deseas cargar desde tu computadora

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_img_2.png" style={{width:600, height:'auto'}}/></div>

**Paso 4.** Requisitos y limitaciones importantes de la imagen:

- Soporta formatos JPG, PNG y GIF
- Las fotos de más de 2MB se comprimirán automáticamente
- Las relaciones de aspecto que no sean 5:3 se ajustarán con relleno blanco
- Resolución objetivo: 800x480 píxeles (o la resolución nativa de tu dispositivo)
- Sin una tarjeta MicroSD, puedes cargar un máximo de 3 fotos
- Con una tarjeta MicroSD, puedes cargar hasta 20 fotos

Paso 5. Selecciona múltiples archivos usando Ctrl/Cmd + Clic si lo deseas

Paso 6. Haz clic en "Abrir" para cargar las imágenes seleccionadas

### Importar imágenes desde URL

**Paso 1.** Haz clic en el botón **Nuevo** en el panel de control<br>
**Paso 2.** En el cuadro de diálogo que aparece, selecciona Galería de imágenes, luego selecciona Importar desde URL<br>
**Paso 3.** Ingresa la URL directa de la imagen en el campo proporcionado<br>
**Paso 4.** Haz clic en "Importar" para agregar la imagen a tu galería

:::tip
Al importar desde URLs, asegúrate de usar enlaces directos de imágenes que terminen con extensiones de archivo como .jpg, .png o .gif. Los enlaces a páginas web que contienen imágenes pueden no funcionar.
:::

## Administrar tu galería

### Configurar el intervalo de visualización

La configuración del intervalo determina cuánto tiempo se muestra cada imagen antes de pasar a la siguiente:

Paso 1. Localiza el campo "Intervalo(min):" en el panel de control

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_1.png" style={{width:600, height:'auto'}}/></div>

Paso 2. Ingresa el tiempo de visualización deseado en minutos (por ejemplo, 1 para un minuto por imagen)

### Elegir el modo de difuminado

El modo de difuminado afecta cómo se procesan las imágenes para una visualización óptima en tu dispositivo específico:

Paso 1. Encuentra el menú desplegable "Modo de difuminado:" en el panel de control
<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_2.png" style={{width:600, height:'auto'}}/></div><br>
Paso 2. Selecciona la opción apropiada para tu dispositivo:

- **Seis colores**: Mejor para pantallas LCD de color, conserva toda la información de color
- **Blanco y negro**: Convierte las imágenes a blanco y negro puro, ideal para pantallas e-paper monocromáticas

:::tip
Para pantallas e-paper/e-ink, selecciona el modo "Blanco y negro" para una calidad de visualización óptima y tasas de actualización más rápidas. Para pantallas LCD, "Seis colores" proporcionará la mejor experiencia visual.
:::

### Usar la barra de herramientas de imagen

Cada imagen en tu galería se puede ajustar usando la barra de herramientas que aparece debajo de la imagen:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_3.png" style={{width:700, height:'auto'}}/></div>

De izquierda a derecha, las herramientas son:

1. **Rellenar horizontalmente**: Ajusta la imagen para llenar la pantalla horizontalmente mientras mantiene la relación de aspecto
2. **Rellenar verticalmente**: Ajusta la imagen para llenar la pantalla verticalmente mientras mantiene la relación de aspecto
3. **Descargar**: Guarda la imagen procesada en tu computadora

:::tip
Usa la opción "Rellenar horizontalmente" para imágenes horizontales y "Rellenar verticalmente" para imágenes verticales para hacer el mejor uso del espacio de tu pantalla mientras evitas la distorsión de la imagen.
:::

### Reordenar imágenes

Puedes cambiar el orden de visualización de tus imágenes usando la tira de miniaturas:

**Paso 1.** Localiza la miniatura de la imagen que deseas mover en la tira en la parte inferior de la pantalla<br>
**Paso 2.** Haz clic y arrastra la miniatura a una nueva posición en la secuencia<br>
**Paso 3.** Suelta para establecer el nuevo orden

## Implementar tu galería en tu dispositivo

Una vez que hayas agregado y configurado tus imágenes, puedes implementar la galería en tu dispositivo conectado:

**Paso 1.** Haz clic en el botón "Guardar" para almacenar tu configuración de galería

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_4.png" style={{width:800, height:'auto'}}/></div>

:::tip
Después de cargar o diseñar una imagen, haz clic habitualmente en el botón guardar para asegurarte de que tu diseño de diseño no se pierda fácilmente.
:::

**Paso 2.** (Opcional) Haz clic en "Vista previa" para ver cómo aparecerá tu galería en el dispositivo sin implementarla completamente

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_5.png" style={{width:800, height:'auto'}}/></div>

**Paso 3.** Haz clic en "Implementar" para enviar tu galería al dispositivo conectado

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_6.png" style={{width:800, height:'auto'}}/></div>

**Paso 4.** Espera el mensaje de confirmación de implementación

:::tip
Después de hacer clic en el botón implementar, es posible que el dispositivo no actualice el álbum de inmediato. El dispositivo puede estar en modo de suspensión. Extraerá las últimas imágenes del álbum cuando se despierte la próxima vez. Si deseas actualizar las fotos de inmediato, puedes hacer clic en el botón verde sobre el dispositivo, y el dispositivo se despertará instantáneamente y extraerá las actualizaciones del panel de control.
:::

Después de la implementación, tu dispositivo comenzará a mostrar las imágenes según tu configuración de intervalo.
Demostración de efecto:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_manage_7.png" style={{width:800, height:'auto'}}/></div>

## Consideraciones de almacenamiento

### Requisitos de tarjeta MicroSD

Para almacenar más de 3 imágenes en tu dispositivo, necesitarás usar una tarjeta MicroSD:

1. **Formato**: La tarjeta MicroSD debe estar formateada como FAT32
2. **Tamaño**: Se recomienda 8GB o más grande (hasta 32GB compatible)
3. **Velocidad**: Se recomienda Clase 10 o superior para un mejor rendimiento

:::tip
El uso de sistemas de archivos distintos a FAT32 puede resultar en que el dispositivo no reconozca la tarjeta MicroSD o no pueda guardar imágenes correctamente.
:::

### Cómo formatear una tarjeta MicroSD como FAT32

- **En Windows:**<br>
    Paso 1. Inserta tu tarjeta MicroSD en tu computadora<br>
    Paso 2. Abre el Explorador de archivos y haz clic derecho en la tarjeta MicroSD<br>
    Paso 3. Selecciona "Formatear..."<br>
    Paso 4. Elige "FAT32" del menú desplegable Sistema de archivos<br>
    Paso 5. Haz clic en "Iniciar" para comenzar el formateo

- **En Mac:**<br>
    Paso 1. Inserta tu tarjeta MicroSD en tu computadora<br>
    Paso 2. Abre Utilidad de Discos (Aplicaciones > Utilidades > Utilidad de Discos)<br>
    Paso 3. Selecciona tu tarjeta MicroSD de la barra lateral<br>
    Paso 4. Haz clic en "Borrar"<br>
    Paso 5. Elige "MS-DOS (FAT)" como formato<br>
    Paso 6. Haz clic en "Borrar" para formatear la tarjeta

### Insertar la tarjeta MicroSD

Paso 1. Apaga tu dispositivo<br>
Paso 2. Localiza la ranura de tarjeta MicroSD en tu dispositivo<br>
Paso 3. Inserta la tarjeta MicroSD correctamente formateada<br>

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/133.jpg" style={{width:700, height:'auto'}}/></div>

Paso 4. Enciende tu dispositivo<br>
Paso 5. Reconecta a SenseCraft HMI para verificar que se reconoce el almacenamiento ampliado

## Optimizar imágenes para tu pantalla

Para obtener los mejores resultados visuales en la pantalla de tu dispositivo:

1. **Coincidir la resolución**: Prepara imágenes que coincidan con la resolución nativa de tu dispositivo (típicamente 800x480 píxeles)
2. **Considera la relación de aspecto**: Usa imágenes con una relación de aspecto 5:3 para evitar el relleno blanco
3. **Optimiza para el tipo de pantalla**:

- Para LCD de color: Las imágenes de color estándar funcionan bien
- Para e-paper/e-ink: Imágenes de mayor contraste con menos gradientes de color
- Para e-paper de 2 colores: Imágenes en blanco y negro o de alto contraste

4. **Tamaño del archivo**: Mantén las imágenes por debajo de 2MB para evitar la compresión automática
5. **Brillo/contraste**: Ajusta según las características específicas de tu pantalla

### Usar herramientas HMI para optimizar la imagen

Puedes elegir la herramienta de imagen de SenseCraft HMI para optimizar tus imágenes. No solo se puede usar para previsualizar tu uso en SenseCraft HMI, sino también generar archivos de encabezado de código C para editar y usar en tu código.
paso 1. En la página [SenseCraft HMI](https://sensecraft.seeed.cc/hmi), selecciona **Herramientas**, y luego elige **Difuminado de imágenes**

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_tools_1.png" style={{width:800, height:'auto'}}/></div>

paso 2. Carga la imagen que deseas optimizar<br>
paso 3. Realiza las modificaciones necesarias según sea necesario.

- Editar imagen: Puede cambiar el tamaño de la imagen
- Tipo de pantalla: Selecciona el tipo de pantalla de tu pantalla
- Personalizado: Basado en el tamaño de la resolución de pantalla que estás usando
- Algoritmo de difuminado: Usa algoritmos para procesar tus imágenes, y soporta una variedad de algoritmos comúnmente usados.
- ID de dispositivo: Tu identificador de dispositivo se usa para distinguir tu dispositivo y se define según tus requisitos de ingeniería.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_tools_2.png" style={{width:800, height:'auto'}}/></div>

paso 4. Selecciona **Vista previa** para ver la imagen mostrada en la pantalla. Dependiendo de tu situación específica, puedes elegir exportar la imagen o generar un archivo de encabezado.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/gallery_tools_3.png" style={{width:800, height:'auto'}}/></div>

## Solución de problemas

### Problemas comunes y soluciones

1. **Las imágenes no se cargan**:

- Verifica que tu imagen esté en un formato compatible (JPG, PNG, GIF)
- Asegúrate de que el tamaño del archivo no sea demasiado grande (idealmente menos de 2MB)
- Intenta con un navegador diferente o borra la caché de tu navegador

2. **No se pueden cargar más de 3 imágenes**:

- Verifica que tengas una tarjeta MicroSD correctamente formateada insertada en tu dispositivo
- Verifica que la tarjeta MicroSD esté formateada como FAT32
- Asegúrate de que el dispositivo esté detectando correctamente la tarjeta MicroSD

3. **Las imágenes se muestran incorrectamente**:

- Ajusta el brillo/contraste usando la barra de herramientas de imagen
- Prepara imágenes que coincidan con la resolución de tu dispositivo

4. **La implementación falla**:

- Asegúrate de que tu dispositivo esté conectado correctamente a SenseCraft HMI
- Verifica que tu dispositivo tenga suficiente espacio de almacenamiento
- Reinicia tu dispositivo e intenta implementar nuevamente

## Conclusión

La función de Galería en SenseCraft HMI proporciona una manera fácil de transformar tus dispositivos con pantalla en marcos de fotos digitales. Siguiendo esta guía, puedes cargar, administrar y mostrar imágenes en tu dispositivo con configuraciones personalizadas para una visualización óptima.

Recuerda que para almacenar más de 3 imágenes, necesitarás una tarjeta MicroSD correctamente formateada insertada en tu dispositivo. Con la configuración correcta, puedes crear hermosas presentaciones de diapositivas y pantallas que muestren tus imágenes favoritas en tus dispositivos de pantalla Seeed Studio.

