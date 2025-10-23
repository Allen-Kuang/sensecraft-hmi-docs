---
title: Interfaz del espacio de trabajo y plantillas
description: Una guía completa para comprender y usar las barras de herramientas principales y las funciones de gestión de páginas en SenseCraft HMI.
---

## Introducción

¡Bienvenido a SenseCraft HMI! Este tutorial será tu guía del sistema nervioso central de la plataforma: las barras de herramientas principales. Dominar estas funciones es la clave para gestionar eficientemente tus proyectos, comprender el estado de tu dispositivo y dar vida a tus diseños.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_28.png" style={{width:400, height:'auto'}}/></div>

Cubriremos tres áreas principales:
1.  **La barra de estado del dispositivo**: Tu fuente de un vistazo para toda la información relacionada con el dispositivo.
2.  **Gestión de páginas y listas de páginas**: El sistema para organizar y crear tu contenido de visualización.
3.  **La barra de herramientas principal**: El conjunto esencial de controles para diseñar, guardar e implementar tu trabajo.

Al final de esta guía, tendrás una comprensión profunda de cómo navegar y controlar el espacio de trabajo de SenseCraft HMI como un profesional.

## La barra de estado del dispositivo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_29.png" style={{width:400, height:'auto'}}/></div>

Ubicada en la parte superior del espacio de trabajo, la Barra de estado del dispositivo proporciona información en tiempo real sobre tu dispositivo conectado.

Desglosemos qué significa cada pieza de información:

*   **Device / e1001**: Esto muestra el nombre y modelo de tu dispositivo actualmente seleccionado.
*   **Sleep**: Esto indica el estado actual del dispositivo. Puede ser "Sleep" (Dormir) o "Awake" (Despierto).
*   **Last Online: 15:27**: Esta marca de tiempo te indica la última vez que el dispositivo se comunicó exitosamente con la plataforma en la nube SenseCraft HMI.
*   **Interval(min): 30**: Esta es una configuración crucial. Define con qué frecuencia (en minutos) el dispositivo se despertará para actualizar su pantalla y obtener nuevos datos o diseños.
*   **Next Online: 15:57**: Basándose en el tiempo "Last Online" y el "Interval", esto predice cuándo el dispositivo se despertará y conectará la próxima vez.
*   **800x480**: Esta es la resolución de pantalla de tu dispositivo conectado. Todos tus diseños en el lienzo se basarán en esta dimensión.
*   **Device Sensor Data**: Para dispositivos compatibles como la serie reTerminal E, esta área muestra lecturas en vivo de los sensores integrados:
    *   🌡️ **26.7**: Temperatura.
    *   💧 **55.9%**: Humedad.
    *   🔋 **100%**: Nivel de batería actual.

:::tip
Para prevenir el quemado de pantalla, especialmente en pantallas e-paper, es altamente recomendable establecer un intervalo de actualización. Actualizar al menos una vez al día puede ayudar a mantener la salud y longevidad de tu pantalla. Un intervalo de `1440` minutos correspondería a una actualización diaria.
:::

## Gestión de páginas y listas de páginas

Esta sección es donde organizas todo el contenido que deseas mostrar en tu dispositivo. Antes de profundizar, es crucial entender dos conceptos clave: **Páginas** y **Listas de páginas**.

*   **Página**: Un diseño de pantalla única. Podría ser un diseño de UI desde Canvas, una imagen de la Galería, un feed RSS o una página Web. Piensa en ella como una sola "diapositiva" en una presentación.
*   **Lista de páginas**: Una colección o "lista de reproducción" de Páginas. Una Lista de páginas puede contener una o más Páginas. Tu dispositivo siempre está configurado para mostrar una Lista de páginas activa. Si la Lista de páginas contiene múltiples Páginas, el dispositivo las recorrerá en el intervalo definido.

:::tip
1. El número máximo de páginas. El límite para imágenes es 20, mientras que otros tipos de página están limitados a 3 cada uno. Las páginas que excedan estos límites no se pueden agregar exitosamente a las Listas de páginas.
:::

### Crear una nueva página

El botón `+ New` es tu punto de partida para agregar nuevo contenido.

**Paso 1.** Haz clic en el botón **+ New**.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_30.png" style={{width:400, height:'auto'}}/></div>

**Paso 2.** Aparecerá un cuadro de diálogo que te dará varias opciones para crear una nueva página:
*   **UI Design (Canvas)**: Crea un diseño personalizado desde cero con varios componentes.
*   **Gallery**: Crea una página para mostrar una imagen.
*   **RSS**: Crea una página para mostrar un feed RSS.
*   **Web**: Crea una página para mostrar una página web.
*   **Templates**: También puedes elegir entre una variedad de plantillas prediseñadas para comenzar con ventaja.

#### Plantillas

Las plantillas proporcionan diseños prediseñados que combinan múltiples componentes en una pantalla cohesiva y lista para usar. Ahorran tiempo y aseguran resultados profesionales sin tener que diseñar diseños desde cero.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_31.png" style={{width:400, height:'auto'}}/></div>

##### Plantilla de visualización del clima

La plantilla de visualización del clima ofrece un panel de clima completo que muestra las condiciones actuales y un pronóstico de 7 días para cualquier ciudad.

Paso 1. Haz clic en la plantilla "Weather Display" en la sección Plantillas

Paso 2. En el cuadro de diálogo "Configure Template: Weather Display" que aparece:

   - Ingresa un nombre de ciudad en el campo "City Name"

   - Haz clic en "Search" para verificar que la ciudad existe en la base de datos del clima

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_32.png" style={{width:400, height:'auto'}}/></div>

Paso 3. Después de una búsqueda exitosa, haz clic en "OK" para continuar

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_33.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Aparecerá una ventana de "Template Preview" que muestra:

   - Panel izquierdo con la fecha actual, condición del clima, temperatura, máxima/mínima y humedad

   - Panel derecho con el nombre de la ciudad y pronóstico de 7 días incluyendo iconos de condiciones y rangos de temperatura

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_34.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Revisa la vista previa y nota:

   - Todos los elementos de la plantilla recibirán IDs únicos para evitar conflictos

   - Puedes modificar la plantilla después de aplicarla al lienzo

Paso 6. Haz clic en "Apply to Canvas" para agregar la plantilla a tu espacio de trabajo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_35.png" style={{width:400, height:'auto'}}/></div>

Paso 7. La plantilla de visualización del clima ahora está en tu lienzo, lista para implementación o personalización adicional

:::note
- La plantilla de visualización del clima usa datos de API del clima en tiempo real que requieren conectividad a internet en tu dispositivo.

- La plantilla es totalmente personalizable después de aplicarse a tu lienzo: puedes redimensionar, reposicionar o modificar cualquier elemento.

- Los datos del clima se actualizan automáticamente según el intervalo de actualización establecido en la configuración de tu proyecto.
:::

##### Plantilla de perfil de GitHub

La plantilla de perfil de GitHub crea un panel completo que muestra la información del perfil de un usuario de GitHub y repositorios seleccionados con sus estadísticas.

Paso 1. Haz clic en la plantilla "GitHub Profile" en la sección Plantillas


Paso 2. En el cuadro de diálogo "Configure Template: GitHub Profile" que aparece:

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_38.png" style={{width:400, height:'auto'}}/></div>

   - Ingresa tu [Token de acceso personal de GitHub](https://github.com/settings/tokens). Es posible que necesites habilitar todos los permisos de usuario para asegurar que el backend de SenseCraft HMI tenga permiso para leer datos del repositorio de código abierto.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_41.png" style={{width:400, height:'auto'}}/></div>

   - Ingresa un nombre de usuario de GitHub en el campo requerido (por ejemplo, "seeed-studio")

   - Opcionalmente ingresa palabras clave en el campo Repository Search para filtrar repositorios

   - Deja el campo de búsqueda vacío para mostrar todos los repositorios del usuario

Paso 3. Haz clic en el botón "Search all '[username]' repositories" para recuperar los repositorios del usuario

Paso 4. De la lista de repositorios mostrados, selecciona hasta 3 repositorios que desees mostrar

   - Cada repositorio muestra su nombre, descripción, lenguaje de programación principal y recuento de estrellas

   - Puedes usar el campo de filtro para reducir la lista de repositorios

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_39.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Haz clic en "OK" para confirmar tus selecciones

Paso 6. Aparecerá una ventana de "Template Preview" que muestra:

   - El nombre para mostrar del usuario de GitHub en la parte superior

   - Etiqueta "Github" con recuento de seguidores

   - Una línea divisoria horizontal

   - Repositorios seleccionados con sus nombres y recuentos de estrellas

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_40.png" style={{width:400, height:'auto'}}/></div>

Paso 7. Revisa la vista previa y nota:

   - La plantilla reemplazará todos los elementos actuales en tu lienzo

   - Todos los elementos de la plantilla recibirán IDs únicos para evitar conflictos

   - Puedes modificar la plantilla después de aplicarla al lienzo

Paso 8. Haz clic en "Apply to Canvas" para agregar la plantilla a tu espacio de trabajo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_42.png" style={{width:400, height:'auto'}}/></div>

:::note
- La plantilla tiene dos modos de búsqueda claramente explicados en la interfaz:

  1. Solo usuario: Ingresa solo el nombre de usuario para mostrar todos los repositorios

  2. Usuario + palabras clave: Ingresa nombre de usuario y palabras clave específicas para filtrar repositorios

- La selección de repositorios está limitada a 3 para asegurar una visualización óptima en pantallas más pequeñas.

- Algunas estadísticas de GitHub pueden estar aproximadas (como recuentos de seguidores de más de 1,000 mostrados como "1.0K").
:::

##### Plantilla de panel de acciones

La plantilla de panel de acciones proporciona una visualización limpia y profesional de datos del mercado de valores en tiempo real, incluyendo precio y cambio porcentual.

Paso 1. Haz clic en la plantilla "Stock Dashboard" en la sección Plantillas

Paso 2. En el cuadro de diálogo "Configure Template: Stock Dashboard" que aparece:

   - Ingresa tu [clave API de Twelve Data](https://sensecraft-hmi-docs.seeed.cc/es/guides/sensecraft-hmi-canvas/#obtener-una-clave-api-de-twelve-data) en el campo proporcionado (enmascarada por seguridad)

Paso 3. La plantilla proporciona cuatro acciones de empresas predeterminadas. Si deseas usar acciones de otras empresas para mostrar, puedes modificarlas tú mismo después de aplicar la plantilla.

Paso 4. Haz clic en "Preview" para confirmar

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_36.png" style={{width:400, height:'auto'}}/></div>

Paso 5. Aparecerá una ventana de "Template Preview" que muestra:

   - Panel izquierdo con el símbolo de la acción en texto grande

   - Panel derecho mostrando el precio actual de la acción y el cambio porcentual

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_37.png" style={{width:400, height:'auto'}}/></div>

Paso 6. Revisa la vista previa y nota:

   - Todos los elementos de la plantilla recibirán IDs únicos para evitar conflictos

   - Puedes modificar la plantilla después de aplicarla al lienzo

Paso 7. Haz clic en "Apply to Canvas" para agregar la plantilla a tu espacio de trabajo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_50.png" style={{width:400, height:'auto'}}/></div>

:::note
- La plantilla de panel de acciones requiere acceso a internet en tu dispositivo para obtener datos del mercado en tiempo real.

- Los datos del mercado de valores se retrasan al menos 15 minutos en el nivel gratuito de Twelve Data.

- Los datos se actualizan según la configuración del intervalo de actualización de tu proyecto.

- Los datos del mercado solo están disponibles durante las horas de negociación de las respectivas bolsas.
:::

##### Plantilla de estadísticas de canal de YouTube

La plantilla de estadísticas de canal de YouTube muestra la marca de un canal de YouTube, eslogan y recuento de suscriptores en un diseño limpio y moderno.

Paso 1. Haz clic en la plantilla "YouTube Channel Stats" en la sección Plantillas

Paso 2. En el cuadro de diálogo "Configure Template: YouTube Channel Stats" que aparece:

   - Ingresa tu [clave API de datos de YouTube](https://sensecraft-hmi-docs.seeed.cc/es/guides/sensecraft-hmi-canvas/#obtener-una-clave-api-de-datos-de-youtube) (enmascarada por seguridad)

   - Ingresa un identificador de canal de YouTube en uno de los formatos compatibles:

     * ID de canal: Cadena de 24 caracteres que comienza con "UC" (por ejemplo, UC_x5XG1OV2P6uZZ5FSM9Ttw)
     * @Handle: Handle del canal que comienza con @ (por ejemplo, @seeedstudiosz)
     * URL del canal: URL completa de YouTube (por ejemplo, youtube.com/@seeedstudiosz)

Paso 3. Haz clic en "Validate Channel" para verificar que el canal existe y recuperar sus datos

Paso 4. Si la validación es exitosa, verás un mensaje de confirmación (por ejemplo, "Found channel: Seeed Studio • 20.4K")

Paso 5. Haz clic en "OK" para continuar

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/125.png" style={{width:800, height:'auto'}}/></div>

Paso 6. Aparecerá una ventana de "Template Preview" que muestra:

   - Panel izquierdo con el nombre del canal y eslogan/descripción en un elegante fondo negro

   - Panel derecho con la etiqueta "YouTube", recuento de suscriptores y texto "Subscribers"

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/126.png" style={{width:800, height:'auto'}}/></div>

Paso 7. Revisa la vista previa y nota:

   - La plantilla reemplazará todos los elementos actuales en tu lienzo

   - Todos los elementos de la plantilla recibirán IDs únicos para evitar conflictos

   - Puedes modificar la plantilla después de aplicarla al lienzo

Paso 8. Haz clic en "Apply to Canvas" para agregar la plantilla a tu espacio de trabajo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/127.png" style={{width:1000, height:'auto'}}/></div>


:::note
- La plantilla de estadísticas de canal de YouTube requiere acceso a internet en tu dispositivo para obtener datos del canal.

- La API de datos de YouTube tiene cuotas y límites de tasa que pueden afectar el uso.

- La plantilla recupera automáticamente el eslogan o descripción del canal cuando esté disponible.

- Para canales con un gran número de suscriptores, el recuento puede ser abreviado (por ejemplo, "1.2M" para 1,200,000).
:::

### Gestión de listas de páginas

El botón **Pagelists** abre una potente interfaz de gestión que te da control total sobre la organización de tu contenido.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_43.png" style={{width:400, height:'auto'}}/></div>

**Paso 1.** Haz clic en el botón **Pagelists** junto al botón `+ New`.

**Paso 2.** Aparecerá el modal "Manage pagelists and pages", que está dividido en tres secciones:

1.  **Pagelists (Panel izquierdo)**: Esta área lista todas las Listas de páginas que has creado.
    *   La lista marcada con estrella (`Default Pagelist` en la imagen) es la que está actualmente activa y se mostrará en el dispositivo.
    *   Puedes hacer clic en `+ New` aquí para crear una nueva Lista de páginas vacía.

2.  **Current Pagelist (Panel central)**: Esto muestra todas las Páginas actualmente dentro de la Lista de páginas seleccionada.
    *   Haz clic en el icono de menos rojo (`-`) para eliminar una página de la Lista de páginas (esto no elimina la página en sí).

3.  **All Pages (Panel derecho)**: Esta es tu biblioteca de todas las Páginas que has creado. Solo aparecerán aquí las páginas donde hayas hecho clic en el botón Guardar.
    *   Para agregar una página a tu Lista de páginas actualmente seleccionada, simplemente haz clic en el icono de más (`+`) en la miniatura de la página deseada. Entonces aparecerá en el panel "Current Pagelist".

**Paso 3.** Una vez que hayas organizado tu Lista de páginas como desees, haz clic en **Confirm** para guardar los cambios.

## La barra de herramientas principal: Tu centro de control

Esta barra de herramientas contiene los botones de acción esenciales para el proceso de diseño e implementación.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_44.png" style={{width:400, height:'auto'}}/></div>

*   **Screen Orientation**: Estos dos iconos te permiten cambiar tu lienzo de diseño entre modos horizontal (horizontal) y vertical (vertical).

*   **Debug (Icono de error)**: Esta es una función poderosa para usuarios avanzados.
    *   Al hacer clic se abre el modal "Debug: Current Layout Data".
    *   Este modal muestra toda la configuración del diseño en formato JSON (JavaScript Object Notation), detallando cada elemento, su posición, tamaño, color y otras propiedades.
    *   Puedes usar esto para comprender la estructura de tu diseño con fines de depuración.
    *   Los usuarios cómodos con código pueden incluso hacer clic en **Manual Edit JSON** para modificar directamente las propiedades del diseño, ofreciendo un grado increíble de control.

    <div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_45.png" style={{width:400, height:'auto'}}/></div>

*   **Import / Export**: Estos botones te permiten guardar tus diseños de página en un archivo local (Export) o cargar un diseño desde un archivo local (Import). Esto es útil para hacer copias de seguridad de tu trabajo o compartir diseños.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/142.png" style={{width:1000, height:'auto'}}/></div>

La función Export te permite guardar tu diseño de UI actual como un archivo:

**Paso 1.** Después de completar tu diseño de interfaz, haz clic en el botón **Export** (icono de flecha hacia afuera) en la barra de herramientas superior.

**Paso 2.** En el cuadro de diálogo de guardar archivo que aparece, elige una ubicación de guardado y nombra tu archivo.

**Paso 3.** Haz clic en "Save" para completar el proceso de exportación.

Tu diseño se guardará como un archivo JSON que contiene toda la información de la interfaz, que se puede usar para copia de seguridad o compartir.

La función Import te permite cargar diseños o plantillas previamente exportados:

**Paso 1.** Haz clic en el botón **Import** (icono de flecha hacia adentro) en la barra de herramientas superior.

**Paso 2.** En el cuadro de diálogo de selección de archivo, localiza y selecciona tu archivo de diseño previamente exportado.

**Paso 3.** Haz clic en "Open" y el diseño seleccionado se cargará en tu espacio de trabajo actual.

:::tip
La operación de importación reemplazará el contenido del espacio de trabajo actual. Se recomienda exportar tu diseño actual antes de importar para prevenir pérdida de datos.
:::

Estas funciones son particularmente útiles para:
- Hacer copias de seguridad de diseños antes de hacer cambios importantes
- Compartir diseños de interfaz con miembros del equipo
- Transferir proyectos entre diferentes dispositivos
- Iniciar rápidamente nuevos proyectos usando plantillas prefabricadas

*   **Save**: Este es uno de los botones más importantes. Guarda tu diseño de página actual en la **nube de SenseCraft HMI**. **No** lo guarda en tu dispositivo.

    :::tip
    Adquiere el hábito de hacer clic en **Save** frecuentemente para asegurar que no pierdas ningún progreso.
    :::

*   **Preview**: Este botón te muestra una vista previa virtual de cómo se verá tu diseño actual en la pantalla del dispositivo. Es una forma rápida y fácil de verificar tu diseño, fuentes y colores sin tener que implementar en el hardware real.

*   **Deploy**: Este es el paso final. El botón **Deploy** envía tu Lista de páginas guardada y activa a tu dispositivo conectado. El dispositivo descargará y mostrará el nuevo contenido.

    :::tip
    Para que la implementación surta efecto inmediatamente, tu dispositivo debe estar despierto. Si el dispositivo está en modo de suspensión, obtendrá el nuevo diseño la próxima vez que se despierte según su horario de intervalo. Puedes despertar manualmente el dispositivo (por ejemplo, presionando un botón en el dispositivo) para activar una actualización y descarga inmediata del diseño implementado.
    :::

## Conclusión

Ahora tienes una comprensión sólida de los controles fundamentales dentro de SenseCraft HMI. Al usar efectivamente la Barra de estado del dispositivo, gestionar tus Páginas y Listas de páginas, y seguir el flujo de trabajo Guardar -> Vista previa -> Implementar, estás bien equipado para crear, gestionar y mostrar cualquier contenido que puedas imaginar en tu dispositivo con pantalla.

