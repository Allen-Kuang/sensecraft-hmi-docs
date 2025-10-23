---
title: Función de diseño de interfaz de usuario
description: Presenta el uso del diseño de interfaz de usuario, una función bajo la plataforma SenseCraft HMI.
---

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/141.jpg" style={{width:800, height:'auto'}}/></div>

## Introducción

La función de diseño de interfaz de usuario en [SenseCraft HMI](https://sensecraft.seeed.cc/hmi) es la característica más potente y flexible de la plataforma, que le permite crear interfaces personalizadas, paneles de control y visualizaciones de datos. Con Canvas, puede diseñar pantallas hermosas que combinan elementos estáticos con datos dinámicos de varias fuentes, incluidos sensores de dispositivos, información meteorológica, datos bursátiles y más.

Esta guía completa le mostrará cómo usar la función de diseño de interfaz de usuario para crear pantallas profesionales para sus dispositivos Seeed. Desde formas básicas y texto hasta widgets de datos en tiempo real y plantillas prediseñadas, aprenderá todo lo que necesita para crear interfaces personalizadas que satisfagan sus necesidades específicas.

Este artículo utilizará el [reTerminal E1002](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/) como ejemplo para explicar cómo usar esta función en la plataforma SenseCraft HMI.

## Primeros pasos con Canvas

### Acceso a la función Canvas

Paso 1. Navegue hasta la plataforma **[SenseCraft HMI](https://sensecraft.seeed.cc/hmi)** a continuación.

Paso 2. Conecte su dispositivo o seleccione un dispositivo ya emparejado para usar.

Paso 3. Si aún no ha creado una página, es posible que deba crear primero una nueva página de diseño de interfaz de usuario.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_1.png" style={{width:1000, height:'auto'}}/></div>

### Comprensión de la interfaz Canvas

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_2.png" style={{width:1000, height:'auto'}}/></div>

La interfaz Canvas consta de varias secciones clave:

1. **Barra lateral de componentes**: Panel izquierdo que contiene todos los elementos disponibles categorizados en Básico, Dispositivo, Datos y Plantillas

2. **Área de diseño de interfaz de usuario**: Espacio de trabajo central donde diseña su interfaz

3. **Barra de herramientas**: Barra superior con herramientas de diseño, configuraciones y opciones de formato

4. **Panel de propiedades**: Aparece cuando se seleccionan elementos, lo que permite la personalización de la apariencia y el comportamiento

5. **Botones de acción**: Botones Guardar, Vista previa e Implementar para probar y aplicar su diseño

## Componentes básicos

La sección Básico proporciona elementos fundamentales para crear el diseño de su interfaz:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_3.png" style={{width:1000, height:'auto'}}/></div>

### Texto

El componente Texto le permite agregar etiquetas, títulos y otro contenido de texto a su lienzo.

Paso 1. Haga clic en el componente "Texto" en la sección Básico. El texto se coloca automáticamente en el centro del lienzo

Paso 2. Arrastre el texto al área donde desea colocarlo

Paso 3. Aparece un cuadro de texto predeterminado con la palabra "Texto"

Paso 4. Use el panel de propiedades para personalizar:

  - Tamaño de fuente (el predeterminado es 30px)

  - Estilo de texto (negrita, cursiva, subrayado)

  - Alineación (izquierda, centro, derecha)

  - Color

  - Familia de fuentes

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_4.png" style={{width:1000, height:'auto'}}/></div>

### Datos

El componente Datos es una herramienta poderosa para mostrar información dinámica obtenida de API externas directamente en su lienzo. Esto le permite integrar datos en tiempo real como clima, precios de acciones o cualquier otra información disponible a través de una API web.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_5.png" style={{width:1000, height:'auto'}}/></div>

Paso 1. Haga clic en el componente "Datos" en la sección Básico. Aparecerá un cuadro de texto de marcador de posición con la palabra "Datos" en el lienzo.

Paso 2. Arrastre el componente "Datos" a la posición deseada.

Paso 3. Con el componente seleccionado, haga clic en el icono **Configuración de datos** (parece un enlace de cadena) en la barra de herramientas para abrir el panel de configuración.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_6.png" style={{width:1000, height:'auto'}}/></div>

Paso 4. En el panel **Configuración de datos**, configure su fuente de datos externa:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_7.png" style={{width:400, height:'auto'}}/></div>

**4.1. Establecer la conexión**

Aquí es donde le dice al componente dónde encontrar su información.

*   **URL de datos remotos:** Ingrese la URL completa del punto final de la API aquí. Por ejemplo, si está construyendo un ticker bursátil, ingresaría la URL proporcionada por su API de datos financieros.
*   **Encabezados de solicitud (opcional):** Algunas API requieren autenticación a través de encabezados. Use el botón **+ Agregar encabezado personalizado** para agregar claves y valores necesarios, como un token de `Autorización`.
*   **Botón de prueba:** Después de ingresar su URL, use siempre el botón **Prueba**. Esto consulta inmediatamente el punto final y le muestra la respuesta JSON sin procesar. Esto es esencial para verificar su conexión y comprender la estructura de datos con la que trabajará.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_8.png" style={{width:400, height:'auto'}}/></div>

Después de hacer clic en el botón Prueba, si la URL se ingresa correctamente, la consola mostrará inmediatamente todos los valores de retorno de los resultados de la prueba. En este punto, puede hacer clic en la entrada deseada con el mouse para obtener directamente el valor específico.

**4.2. Extraer el valor específico**

Una respuesta de API a menudo contiene muchos datos, pero generalmente solo necesita una parte de ellos.

*   **Clave de datos:** Use la notación de puntos para especificar la ruta exacta a los datos que desea mostrar. Si su API devuelve `{"stock":{"price": 150.75}}`, su clave de datos sería `stock.price` para extraer el precio. Para datos en matrices, use la notación de corchetes como `forecast[0].temperature`.
*   **Precisión:** Para datos numéricos, esta configuración controla el número de decimales que se muestran. Establecerlo en `2` formateará `150.7531` como `150.75`.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_9.png" style={{width:400, height:'auto'}}/></div>

**4.3. Transformar los datos para la visualización**

Esta sección es en realidad un módulo independiente. No tiene conexión inherente con las secciones 4.1 y 4.2. Proporciona un conjunto de valores de datos predefinidos, potencialmente utilizados con frecuencia, lo que permite a los usuarios aplicarlos directamente sin necesidad de localizar la API ellos mismos.

Estos son los transformadores integrados que puede seleccionar:

*   **Ninguno - Sin transformación:** Muestra el valor extraído sin procesar.
*   **Formato de fecha:** Convierte una marca de tiempo de computadora (por ejemplo, `1678886400`) en una fecha legible por humanos (por ejemplo, "2023-03-15").
*   **Función personalizada:** La herramienta definitiva para la flexibilidad. Escriba su propio JavaScript para manipular el valor. Por ejemplo, `return '$' + value;` agregaría un signo de dólar como prefijo al precio de una acción.
*   **Código meteorológico a descripción:** Una función especializada que traduce códigos meteorológicos numéricos de una API en texto descriptivo como "Soleado" o "Lluvia".
*   **Estado del nivel de batería:** Convierte inteligentemente un porcentaje (0-100) en un estado como "Alto", "Medio" o "Bajo".
*   **Formato de número grande:** Acorta automáticamente números grandes para facilitar la lectura (por ejemplo, `1250000` se convierte en "1.25M").
*   **Tiempo relativo:** Transforma una marca de tiempo en una expresión relativa como "Actualizado hace 5 minutos", haciendo que sus datos se sientan más inmediatos.

Al combinar estas configuraciones, puede controlar con precisión cómo se obtienen, interpretan y presentan los datos externos en su lienzo, creando una pantalla verdaderamente dinámica e informativa.

Paso 5. También puede personalizar la apariencia de los datos mostrados utilizando el panel de propiedades para ajustar:
  - Tamaño y estilo de fuente
  - Alineación
  - Color
  - Familia de fuentes

### Imagen

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_10.png" style={{width:400, height:'auto'}}/></div>

El componente Imagen le permite agregar imágenes a su lienzo. Puede elegir cargar localmente o usar un enlace de imagen.

Paso 1. Haga clic en el componente "Imagen"

Paso 2. En el panel de propiedades, haga clic en "Cargar" para agregar su imagen o ingrese una URL de imagen

Paso 3. Ajuste el tamaño y la posición según sea necesario

### Fecha

El componente Fecha muestra una fecha, hora o marca de tiempo que se puede configurar en varios formatos.

Paso 1. Haga clic en el componente "Fecha" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con un formato de fecha predeterminado (generalmente MM/DD/AAAA)

Paso 3. Haga clic en el icono del calendario en la barra de herramientas para abrir el panel de Configuración de fecha

Paso 4. En el panel de Configuración de fecha:

   - Establezca una fecha específica utilizando el selector de fecha o el campo de entrada

   - Seleccione un formato de fecha del menú desplegable (por ejemplo, MM/DD/AAAA, DD/MM/AAAA, AAAA-MM-DD)

   - Seleccione su zona horaria en la sección Zona horaria.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_11.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Use el panel de propiedades para personalizar aún más:

   - Tamaño y estilo de fuente

   - Color de texto

   - Alineación

   - Fondo (si lo desea)

:::note
Dentro de la Configuración de datos, hay un interruptor Usar hora actual. De forma predeterminada, el interruptor muestra APAGADO, lo que indica que el dispositivo actualizará automáticamente la hora de este componente en función de la hora real. Cuando presiona el botón APAGADO, esta función se desactiva y la hora no se actualizará automáticamente, en su lugar mostrará un valor fijo.
:::

### Formas

SenseCraft HMI Canvas ofrece varios componentes de forma:

- **Rectángulo**: Crea un rectángulo o cuadrado estándar

- **Rectángulo redondeado**: Crea un rectángulo con esquinas redondeadas

- **Círculo**: Crea un círculo perfecto

- **Elipse**: Crea una forma ovalada

- **Triángulo**: Crea una forma de tres lados

- **Polígono**: Crea formas de múltiples lados

- **Línea**: Crea líneas rectas

- **Dibujo**: Habilita el dibujo a mano alzada

Para cada forma:

Paso 1. Haga clic en el componente de forma deseado

Paso 2. Haga clic y arrastre en el lienzo para determinar la ubicación final

Paso 3. Use el panel de propiedades para personalizar:

  - Color de relleno

  - Color y ancho del borde

  - Opacidad

  - Radio de esquina (para rectángulos)

  - Otras propiedades específicas de la forma

### Código QR

El componente Código QR genera un código QR (Respuesta Rápida) escaneable de cualquier texto o URL que proporcione.

Paso 1. Haga clic en el componente "Código QR" en la sección Dibujo de la lista de componentes.

Paso 2. El componente se colocará en su lienzo con un código QR predeterminado.

Paso 3. Haga clic en el icono QR en la barra de herramientas del componente para abrir el panel de Contenido del código QR.

Paso 4. En el panel de contenido, ingrese el texto o la URL que desea codificar en el campo de entrada "Contenido del código QR". El código QR en el lienzo se actualizará automáticamente a medida que escribe.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_26.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Use el panel de propiedades para personalizar aún más el tamaño y la posición del componente en el lienzo.

### Código de barras

El componente Código de barras genera un código de barras estándar escaneable a partir de texto o números.

Paso 1. Haga clic en el componente "Código de barras" en la sección Dibujo de la lista de componentes.

Paso 2. El componente se colocará en su lienzo con un código de barras predeterminado y sus números correspondientes mostrados debajo.

Paso 3. Haga clic en el icono de Barra en la barra de herramientas del componente para abrir el panel de Contenido del código de barras.

Paso 4. En el panel de contenido, ingrese el texto o los números que desea codificar en el campo de entrada "Contenido del código de barras". El código de barras y el texto debajo se actualizarán automáticamente.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_27.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Use el panel de propiedades para personalizar aún más el tamaño y la posición del componente en el lienzo.

## Componentes del dispositivo

La sección Dispositivo contiene componentes que muestran automáticamente datos de los sensores de su dispositivo de pantalla ePaper de la serie reTerminal E de Seeed conectado:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_12.png" style={{width:400, height:'auto'}}/></div>

### Componente de batería

El componente de Batería muestra el nivel de batería actual de su dispositivo conectado.

Paso 1. Haga clic en el componente "Batería"

Paso 2. El componente mostrará automáticamente el porcentaje de batería de su dispositivo

Paso 3. Use el panel de propiedades para personalizar:

  - Tamaño de fuente (el predeterminado es 30px)

  - Estilo de texto (negrita, cursiva, subrayado)

  - Alineación (izquierda, centro, derecha)

  - Color

  - Familia de fuentes

### Componente de temperatura

El componente de Temperatura muestra la lectura de temperatura actual del sensor de su dispositivo.

Paso 1. Haga clic en el componente "Temperatura"

Paso 2. El componente mostrará automáticamente la lectura de temperatura de su dispositivo

Paso 3. Use el panel de propiedades para personalizar:

  - Tamaño de fuente (el predeterminado es 30px)

  - Estilo de texto (negrita, cursiva, subrayado)

  - Alineación (izquierda, centro, derecha)

  - Color

  - Familia de fuentes

### Componente de humedad

El componente de Humedad muestra la lectura de humedad actual del sensor de su dispositivo.

Paso 1. Haga clic en el componente "Humedad"

Paso 2. El componente mostrará automáticamente el porcentaje de humedad de su dispositivo

Paso 3. Use el panel de propiedades para personalizar:

  - Tamaño de fuente (el predeterminado es 30px)

  - Estilo de texto (negrita, cursiva, subrayado)

  - Alineación (izquierda, centro, derecha)

  - Color

  - Familia de fuentes

### Componente SenseCAP

Si ha comprado previamente un sensor SenseCAP, SenseCraft-HMI ahora admite la recuperación directa de lecturas de sensores de nodos SenseCAP en su cuenta.

Paso 1. Haga clic en el componente "SenseCAP"

Paso 2. Los componentes se colocarán automáticamente en el centro del lienzo

Paso 3. Seleccione los valores del sensor que desea mostrar en el panel de Propiedades.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_13.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Use el panel de propiedades para personalizar:

  - Tamaño de fuente (el predeterminado es 30px)

  - Estilo de texto (negrita, cursiva, subrayado)

  - Alineación (izquierda, centro, derecha)

  - Color

  - Familia de fuentes

## Componentes de datos

La sección Datos contiene componentes que se conectan a fuentes de datos externas para mostrar información como clima, acciones y más:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/96.png" style={{width:400, height:'auto'}}/></div>

### Clima

El componente Clima muestra información meteorológica actual para una ubicación especificada.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_14.png" style={{width:400, height:'auto'}}/></div>

Paso 1. Haga clic en el componente "Clima" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con la Temperatura predeterminada

Paso 3. Usando la barra de herramientas en la parte superior, configure las opciones de visualización del clima:

   - Seleccione una ubicación (por ejemplo, "Nueva York") del campo de ubicación

   - Elija qué datos meteorológicos mostrar del menú desplegable:

     * Clima actual (temperatura, condiciones)

     * Hoy (pronóstico de hoy)

     * Día 2 hasta Día 7 (pronósticos futuros)

Paso 4. Use el panel de propiedades para personalizar aún más la apariencia

### Icono del clima

El componente Icono del clima muestra una representación visual de las condiciones climáticas actuales.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_15.png" style={{width:400, height:'auto'}}/></div>

Paso 1. Haga clic en el componente "Icono del clima" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo

Paso 3. Usando la barra de herramientas en la parte superior, seleccione la ubicación (por ejemplo, "Nueva York") del campo de ubicación

Paso 4. Use el panel de propiedades para personalizar:
   - Tamaño y posición
   - Estilo de icono

### GitHub

El componente GitHub muestra información sobre un perfil de usuario de GitHub.

Paso 1. Haga clic en el componente "GitHub" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con el texto predeterminado que muestra "Seeed Studio"

Paso 3. En la barra de herramientas, verá un campo de nombre de usuario de GitHub (por ejemplo, "seeed-studio") y un menú desplegable

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_16.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Aquí, necesita [solicitar un Token desde su cuenta de GitHub](https://github.com/settings/tokens). SenseCraft HMI usará este Token para recuperar información relacionada con el nombre de GitHub que proporcionó para fines de visualización. Luego ingrese un nombre de usuario de GitHub válido en el campo y haga clic en "Validar" en el panel de Configuración de usuario de GitHub que aparece.

Paso 5. Del menú desplegable etiquetado como "Nombre para mostrar" (o similar), seleccione qué información de usuario de GitHub desea mostrar:

   - Nombre para mostrar (muestra el nombre para mostrar del usuario)

   - Nombre de usuario (muestra el identificador de GitHub del usuario)

   - Seguidores (muestra el número de seguidores)

   - Siguiendo (muestra el número de usuarios seguidos)

   - Repositorios públicos (muestra el número de repositorios públicos)

   - Gists públicos (muestra el número de gists públicos)

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_18.png" style={{width:400, height:'auto'}}/></div>

Paso 6. Use el panel de propiedades para personalizar la apariencia del componente GitHub

:::note
- El componente GitHub requiere acceso a Internet en su dispositivo para obtener datos de GitHub en tiempo real.

- La API de GitHub tiene límites de velocidad, por lo que la actualización excesiva puede deshabilitar temporalmente el componente.
:::

:::tip
Pruebe estos nombres de usuario de GitHub para probar:

- seeed-studio (GitHub oficial de Seeed Studio)

- torvalds (Linus Torvalds, creador de Linux)

- microsoft (GitHub oficial de Microsoft)

- google (GitHub oficial de Google)
:::

### Repositorio de GitHub

El componente Repositorio de GitHub muestra información sobre un repositorio específico de GitHub.

Paso 1. Haga clic en el componente "Repositorio de GitHub" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con el texto predeterminado que muestra "wiki-documents"

Paso 3. En el panel de Configuración del repositorio de GitHub que aparece:

   - Puede ver el estado actual del usuario y el repositorio

   - Busque repositorios ingresando palabras clave o dejando el campo vacío para mostrar todos los repositorios de un usuario

   - Ingrese manualmente un repositorio específico en el formato "Nombre de usuario/Repositorio" (por ejemplo, "Seeed-Studio/wiki-documents")

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_17.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Haga clic en "Buscar" para encontrar y validar el repositorio

Paso 5. Del menú desplegable en la barra de herramientas, seleccione qué información del repositorio desea mostrar:

   - Nombre (muestra el nombre del repositorio)

   - Nombre completo (muestra el formato nombre de usuario/repositorio)

   - Estrellas (muestra el número de estrellas)

   - Bifurcaciones (muestra el número de bifurcaciones)

   - Observadores (muestra el número de observadores)

   - Descripción (muestra la descripción del repositorio)

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_20.png" style={{width:400, height:'auto'}}/></div>

Paso 6. Use el panel de propiedades para personalizar la apariencia del componente Repositorio de GitHub

:::note
- Al igual que el componente de usuario de GitHub, el componente Repositorio de GitHub requiere acceso a Internet en su dispositivo para obtener datos.

- La API de GitHub tiene límites de velocidad que pueden afectar la frecuencia con la que se pueden actualizar los datos.
:::

### Acciones

El componente Acciones muestra información del mercado de valores en tiempo real para símbolos especificados.

Paso 1. Haga clic en el componente "Acciones" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con un texto predeterminado "AAPL" (símbolo de acciones de Apple)

Paso 3. Haga clic en el botón "Configurar" en la barra de herramientas para abrir el panel de Configuración de acciones

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_19.png" style={{width:400, height:'auto'}}/></div>

Paso 4. En el panel de Configuración de acciones:

   - Ingrese un símbolo de acción (por ejemplo, "AAPL", "MSFT", "GOOGL") en el campo Símbolo de acción

   - Haga clic en "Buscar" para validar el símbolo

   - Ingrese su clave API de Twelve Data en el campo proporcionado (Puede consultar el tutorial [a continuación](#obtener-una-clave-api-de-twelve-data) para aprender cómo obtener la API)

Paso 5. Del menú desplegable "Símbolo" en la barra de herramientas, seleccione qué datos de acciones mostrar:

   - Símbolo (solo muestra el símbolo del ticker de acciones)

   - Precio actual (muestra el último precio de la acción)

   - Cambio (muestra el cambio de precio desde el cierre anterior)

   - Porcentaje de cambio (muestra el porcentaje de cambio)

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_21.png" style={{width:400, height:'auto'}}/></div>

Paso 6. Use el panel de propiedades para personalizar la apariencia del componente de acciones

#### Obtener una clave API de Twelve Data

Para usar el componente Acciones, necesitará una clave API gratuita de Twelve Data:

Paso 1. Visite [twelvedata.com](https://twelvedata.com/)

Paso 2. Haga clic en "Comenzar gratis" o "Registrarse"

Paso 3. Cree una cuenta con su dirección de correo electrónico y contraseña

Paso 4. Una vez registrado e iniciado sesión, navegue a su panel

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/103.png" style={{width:1000, height:'auto'}}/></div>

Paso 5. Localice y copie su clave API

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/104.png" style={{width:800, height:'auto'}}/></div>

Paso 6. Pegue esta clave API en el campo "Clave API de Twelve Data" en el panel de Configuración de acciones

:::note
- El nivel gratuito de Twelve Data permite un número limitado de llamadas API por minuto y por día.

- Los datos de acciones que se muestran en Canvas son solo para fines de visualización. La información de acciones en tiempo real solo se mostrará después de implementar el diseño en su dispositivo, que luego obtendrá los datos actuales de los servidores de Twelve Data.

- Para la experiencia más confiable, considere actualizar a un plan pago de Twelve Data si necesita actualizaciones frecuentes de acciones.
:::

:::tip
Para fines de prueba, puede usar símbolos de acciones comunes como:

- AAPL (Apple)

- MSFT (Microsoft)

- GOOGL (Alphabet/Google)

- AMZN (Amazon)

- TSLA (Tesla)
:::

### YouTube

El componente YouTube muestra información y estadísticas sobre un canal de YouTube.

Paso 1. Haga clic en el componente "YouTube" en la sección Datos

Paso 2. El componente se colocará automáticamente en el centro de su lienzo con el texto predeterminado que muestra "SeeedStudio"

Paso 3. En el panel de Configuración de YouTube que aparece:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_22.png" style={{width:400, height:'auto'}}/></div>

   - Ingrese un ID de canal de YouTube (por ejemplo, "UC_x5XG1OV2P6uZZ5FSM9Ttw") en el campo Canal de YouTube

   - Haga clic en "Buscar" para validar el canal

   - Ingrese su clave API de datos de YouTube en el campo proporcionado

   - Haga clic en el enlace "Consola de Google Cloud" para [obtener una clave API gratuita](#obtener-una-clave-api-de-datos-de-youtube) si no tiene una

Paso 4. Del menú desplegable en la barra de herramientas, seleccione qué información del canal desea mostrar:

   - Nombre del canal (muestra el nombre del canal de YouTube)

   - ID del canal (muestra el ID del canal de YouTube)

   - Descripción (muestra la descripción del canal)

   - Suscriptores (muestra el recuento de suscriptores)

   - Vistas (muestra el recuento total de vistas)

   - Videos (muestra el número de videos cargados)

   - Publicado en (muestra la fecha de creación del canal)

   - URL personalizada (muestra la URL personalizada si está disponible)

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_23.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Use el panel de propiedades para personalizar la apariencia del componente YouTube

#### Obtener una clave API de datos de YouTube

:::note
Si no sabe cómo obtener una clave API, también puede leer [la documentación oficial de Google](https://developers.google.com/youtube/v3/getting-started).
:::

Para usar el componente YouTube, necesitará una clave API gratuita de la Consola de Google Cloud:

Paso 1. Visite [Consola de Google Cloud](https://console.cloud.google.com/)

Paso 2. Cree un nuevo proyecto o seleccione uno existente

Paso 3. Navegue a "API y servicios" > "Biblioteca"

Paso 4. Busque "YouTube Data API v3" y habilítelo

Paso 5. Vaya a "API y servicios" > "Credenciales"

Paso 6. Haga clic en "Crear credenciales" > "Clave API"

Paso 7. Copie su nueva clave API

Paso 8. Pegue esta clave API en el campo "Clave API de datos de YouTube" en el panel de Configuración de YouTube

:::note
- El componente YouTube requiere acceso a Internet en su dispositivo para obtener datos del canal.

- Canvas muestra "No se configuró la clave API" hasta que proporcione una clave API válida y un ID de canal.

- La API de datos de YouTube de Google tiene cuotas y límites de velocidad que pueden afectar el uso.

- Algunas estadísticas (como recuentos exactos de suscriptores) pueden ser redondeadas o aproximadas según las políticas de YouTube.
:::

### Generador de diseño con IA

SenseCraft HMI Canvas incluye un generador de diseño impulsado por IA:

Paso 1. Haga clic en el botón "Generador de IA" en la parte superior derecha

Paso 2. Ingrese una descripción del diseño que desea crear

Paso 3. Haga clic en "Generar" para que la IA cree un diseño basado en su descripción

Paso 4. Personalice el diseño generado según sea necesario

Esta función es excelente para crear diseños rápidamente sin empezar desde cero.

:::tip
Para obtener instrucciones detalladas sobre el uso de esta sección, consulte **[Uso de la generación con IA en SenseCraft HMI](https://sensecraft-hmi-docs.seeed.cc/en/guides/sensecraft-hmi-ai-generator/)**.
:::

## Implementación en su dispositivo

Una vez que haya creado su diseño de lienzo, querrá implementarlo en su dispositivo Seeed:

### Vista previa antes de la implementación

Paso 1. Haga clic en el botón "Vista previa" en la barra de herramientas superior

Paso 2. Revise cómo aparecerá su diseño en el dispositivo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_24.png" style={{width:400, height:'auto'}}/></div>

Paso 3. Realice los ajustes necesarios

### Guardar su diseño

Paso 1. Haga clic en el botón "Guardar" para almacenar su diseño actual

Paso 2. Su diseño se guardará en la nube de SenseCraft HMI

### Implementar en el dispositivo

Paso 1. Asegúrese de que su dispositivo esté conectado y muestre el estado "En línea"

Paso 2. Haga clic en el botón "Implementar"

Paso 3. Espere a que se complete el proceso de implementación

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_25.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Su diseño aparecerá en su dispositivo conectado

### Consideraciones de implementación

Para una implementación exitosa en dispositivos Seeed:

1. **Compatibilidad del dispositivo**: Asegúrese de que su diseño esté optimizado para la resolución de pantalla específica de su dispositivo

2. **Estado de conexión**: Asegúrese de que su dispositivo muestre el estado "En línea" antes de implementar

3. **Componentes de datos**: Si usa componentes de datos (Clima, Acciones, etc.), asegúrese de que su dispositivo tenga conectividad a Internet

4. **Sensores del dispositivo**: Los componentes como Batería, Temperatura y Humedad solo funcionarán con dispositivos compatibles de pantalla ePaper de la serie reTerminal E de Seeed que tengan los sensores apropiados

5. **Frecuencia de actualización**: Establezca un tiempo de intervalo apropiado según la frecuencia con la que necesita actualizar sus datos y las capacidades de su dispositivo

## Solución de problemas

### Problemas comunes de Canvas y soluciones

1. **Los componentes no muestran datos**:
   - Verifique la conexión a Internet de su dispositivo
   - Verifique que la fuente de datos esté disponible
   - Asegúrese de que la ruta de la clave de datos sea correcta para los componentes dinámicos
   - Intente actualizar el lienzo o volver a implementar

2. **Problemas de diseño en el dispositivo**:
   - Use la función Vista previa para probar antes de la implementación
   - Evite colocar elementos demasiado cerca de los bordes del lienzo

3. **La implementación falla**:
   - Asegúrese de que su dispositivo esté conectado correctamente a SenseCraft HMI
   - Verifique la conexión a Internet de su dispositivo
   - Intente guardar su diseño y luego implementarlo nuevamente
   - Reinicie su dispositivo e intente implementarlo nuevamente

4. **Los datos del sensor del dispositivo no se muestran**:
   - Verifique que su dispositivo tenga los sensores requeridos
   - Verifique que el firmware de su dispositivo esté actualizado
   - Asegúrese de que el dispositivo esté conectado correctamente a SenseCraft HMI

5. **El texto o las imágenes aparecen distorsionados**:
   - Ajuste el tamaño y la posición de los componentes
   - Verifique la configuración de fuente para los componentes de texto
   - Para las imágenes, asegúrese de que tengan una resolución apropiada para su pantalla

## Conclusión

La función Canvas en SenseCraft HMI proporciona una plataforma poderosa para crear interfaces personalizadas y paneles de control para sus dispositivos Seeed. Al combinar elementos de diseño básicos con componentes de datos dinámicos y plantillas prediseñadas, puede crear pantallas de aspecto profesional que sirven para una amplia gama de propósitos.

Ya sea que esté construyendo una estación meteorológica, monitor de dispositivos, pantalla de información o panel de control, Canvas le brinda las herramientas para dar vida a su visión. La interfaz intuitiva de arrastrar y soltar combinada con funciones avanzadas como el enlace de datos dinámicos y las herramientas de depuración la hace accesible para principiantes y al mismo tiempo ofrece la profundidad que necesitan los usuarios experimentados.


