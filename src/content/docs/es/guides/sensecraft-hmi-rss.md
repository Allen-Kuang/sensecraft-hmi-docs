---
title: Función RSS
description: Presenta el uso de RSS, una función de la plataforma SenseCraft HMI.
---

# Uso de RSS en SenseCraft HMI

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/80.jpg" style={{width:800, height:'auto'}}/></div>

## Introducción

La función RSS en [SenseCraft HMI](https://sensecraft.seeed.cc/hmi) te permite transformar tus dispositivos con pantalla en pantallas de información en tiempo real. Al conectarte a feeds RSS de medios de noticias, blogs, servicios meteorológicos y más, puedes crear pantallas dinámicas que se actualizan automáticamente con el contenido más reciente. Esta función es perfecta para crear tickers de noticias, tableros de información o paneles personales que te mantienen informado sin intervención manual.

Este tutorial te guiará para comprender los feeds RSS y usar la función RSS en SenseCraft HMI para mostrar contenido en tu dispositivo.

Este artículo utilizará el [reTerminal E1002](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/) como ejemplo para explicar cómo usar esta función en la plataforma SenseCraft HMI.

## Comprender RSS

### ¿Qué es RSS?

RSS (Really Simple Syndication) es un formato de feed web estandarizado utilizado para publicar contenido actualizado con frecuencia como:

- Artículos de noticias
- Publicaciones de blog
- Podcasts
- Actualizaciones de video
- Pronósticos del tiempo
- Datos del mercado de valores

Los feeds RSS permiten a los usuarios mantenerse actualizados sin tener que visitar cada sitio web individualmente. En su lugar, el nuevo contenido se entrega automáticamente a tu lector RSS o, en este caso, a tu dispositivo habilitado para SenseCraft HMI.

### Cómo funciona RSS

1. **Los editores de contenido** (sitios web, blogs, medios de noticias) crean feeds RSS que contienen su contenido más reciente en un formato XML estandarizado<br>
2. **Los lectores de feeds** (como la función RSS en SenseCraft HMI) verifican regularmente estos feeds para actualizaciones<br>
3. Cuando se publica nuevo contenido, el lector de feeds **recupera y muestra** las actualizaciones

### Beneficios de usar RSS

- **Actualizaciones en tiempo real**: Obtén la información más reciente sin actualización manual
- **Agregación de contenido**: Combina múltiples fuentes en una sola pantalla
- **Información filtrada**: Recibe solo el contenido que te interesa
- **Eficiencia de ancho de banda**: Los feeds RSS contienen solo contenido esencial, no páginas web completas
- **Sin publicidad**: RSS típicamente entrega contenido limpio sin anuncios

## Primeros pasos

### Acceder a la función RSS

Paso 1. Navega a la plataforma SenseCraft HMI a continuación.<br>
    [SenseCraft HMI](https://sensecraft.seeed.cc/hmi)<br>
Paso 2. Conecta tu dispositivo o selecciona un dispositivo ya emparejado para usar.<br>
Paso 3. Haz clic en la opción **Noticias RSS**
<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/rss_start_1.png" style={{width:1000, height:'auto'}}/></div>

paso 4. Importa URL, por ejemplo

```url
https://feeds.bbci.co.uk/news/world/rss.xml
```

### Comprender la interfaz RSS

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/rss_start_2.png" style={{width:1000, height:'auto'}}/></div>

La interfaz RSS consta de dos secciones principales:

1. **Panel de configuración**: Ubicado en la parte superior, donde puedes ingresar y validar URLs de feeds RSS<br>
2. **Área de visualización**: La sección principal donde se mostrará el contenido RSS después de la configuración<br>

## Configurar feeds RSS

### Agregar un feed RSS

Paso 1. Localiza el panel de Configuración RSS en la parte superior de la pantalla, Encuentra el campo de entrada **URL RSS**<br>
Paso 2. Ingresa una URL de feed RSS válida en el campo (por ejemplo, https://news.google.com/rss)<br>
Paso 3. Haz clic en el botón **Establecer** para validar y aplicar el feed RSS, Si la URL es válida, el sistema comenzará a recuperar y mostrar contenido del feed

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/rss_url_1.png" style={{width:1000, height:'auto'}}/></div>

### Configuración y personalización de visualización

Una vez que tu feed RSS esté configurado, puedes ajustar cómo se muestra el contenido:
Paso 1. Usa la misma configuración de intervalo y modo de difuminado que se encuentra en la función de Galería:

- **Intervalo(min)**: Establece con qué frecuencia la pantalla se actualiza con nuevo contenido
- **Modo de difuminado**: Elige entre "Color completo" o "Blanco y negro" según el tipo de pantalla

Paso 2. Haz clic en **Guardar** para almacenar tu configuración<br>
Paso 3. Haz clic en **Vista previa** para ver cómo se mostrará el contenido RSS en tu dispositivo<br>
Paso 4. Haz clic en **Implementar** para enviar la configuración a tu dispositivo conectado<br>

## Encontrar y usar feeds RSS

### Fuentes populares de feeds RSS

Aquí hay algunos feeds RSS populares y confiables que puedes usar con SenseCraft HMI:

**Noticias:**

- BBC News:  https://feeds.bbci.co.uk/news/world/rss.xml <br>
- Reuters:  https://www.reutersagency.com/feed/ <br>
- CNN:  https://rss.cnn.com/rss/edition.rss <br>
- The New York Times:  https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml

**Tecnología:**

- Wired:  https://www.wired.com/feed/rss <br>
- TechCrunch:  https://techcrunch.com/feed/ <br>
- Ars Technica:  https://feeds.arstechnica.com/arstechnica/index <br>
- Hackaday:  https://hackaday.com/blog/feed/

**Clima:**

- National Hurricane Center: https://www.nhc.noaa.gov/index-at.xml

**Ciencia:**

- NASA Breaking News:  https://www.nasa.gov/rss/dyn/breaking_news.rss <br>
- Science Daily:  https://www.sciencedaily.com/rss/all.xml

### Cómo encontrar feeds RSS para sitios web

Muchos sitios web ofrecen feeds RSS, pero no siempre son fáciles de encontrar. Aquí hay algunos métodos para localizar feeds RSS:

- **Método 1**: Busca iconos RSS<br>
    Muchos sitios web muestran un icono RSS (generalmente naranja) o enlaces etiquetados como "RSS", "Feed" o "Suscribirse" en su pie de página o barra lateral.

- **Método 2**: Agrega "/feed" a las URLs de blogs<br>
    Para muchos sitios basados en WordPress, agregar "/feed" al final de la URL a menudo funciona:<br>
    ```
    https://example.com/feed
    ```
- **Método 3**: Usa extensiones de navegador<br>
    Las extensiones de navegador como "RSS Feed Reader" para Chrome o "Awesome RSS" para Firefox pueden detectar feeds disponibles en los sitios web que visitas.

    <div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/81.png" style={{width:1000, height:'auto'}}/></div>

- **Método 4**: Revisa el código fuente<br>
    1. Visita el sitio web
    2. Haz clic derecho y selecciona "Ver código fuente de la página"
    3. Busca (Ctrl+F) "rss" o "feed"
    4. Busca enlaces con "application/rss+xml" en el atributo type
    
- **Método 5**: Usa buscadores de feeds RSS<br>
    Servicios como:<br>
    - [Feed Finder](https://feedfinder.mackerron.com/)<br>
    - [RSS.app](https://rss.app/rss-feed)<br>
    Estos pueden ayudar a descubrir feeds RSS para sitios web que no los anuncian prominentemente.

## Crear feeds RSS personalizados

Si no puedes encontrar un feed RSS para el contenido que deseas mostrar, puedes crear el tuyo propio usando varias herramientas:

### Servicios de creación de feeds RSS

1. **RSS.app**: https://rss.app/

    - Crea feeds RSS desde sitios web, redes sociales u otras fuentes
    - No se requiere codificación
    - Opciones gratuitas y de pago disponibles

2. **Feedly**: https://feedly.com/

    - Crea tableros de contenido que se pueden exportar como RSS
    - Bueno para curación de contenido

3. **Zapier**: https://zapier.com/

    - Crea flujos de trabajo automatizados que pueden generar feeds RSS desde varios desencadenantes
    - Requiere una suscripción de pago para funciones avanzadas

### Agregadores de feeds

También puedes combinar múltiples feeds RSS en un solo feed usando agregadores:

1. **FeedBlendr**: http://feedblendr.com/

    - Combina múltiples feeds en uno
    - Simple de usar

2. **RSSMix**: http://www.rssmix.com/

    - Fusiona múltiples feeds RSS
    - Servicio gratuito

## Consejos avanzados de visualización RSS

### Optimizar el contenido RSS para tu pantalla

Para la mejor experiencia con feeds RSS en tu dispositivo SenseCraft HMI:

1. **Elige feeds con longitud de contenido apropiada**:

    - Los feeds con títulos y descripciones cortos funcionan mejor para pantallas pequeñas
    - Los feeds de artículos completos pueden ser demasiado pesados en texto para pantallas e-paper

2. **Considera la frecuencia de actualización**:

    - Ajusta tu configuración de intervalo a la frecuencia de actualización del feed
    - Los feeds de noticias pueden actualizarse cada hora, mientras que los feeds de blogs pueden actualizarse diariamente

3. **Prueba diferentes modos de difuminado**:

    - El modo "Blanco y negro" funciona mejor para feeds RSS con mucho texto en pantallas e-paper
    - "Color completo" es mejor para feeds con imágenes en pantallas LCD

4. **Ten en cuenta el contenido de imagen**:

    - Algunos feeds RSS incluyen imágenes que pueden no mostrarse bien en todos los dispositivos
    - Los feeds con imágenes grandes pueden cargarse más lentamente

## Solución de problemas

### Problemas comunes de RSS y soluciones

1. **Error "Feed RSS no válido"**:

    - Verifica que la URL sea correcta e incluya el prefijo http:// o https://
    - Verifica si el feed es accesible pegando la URL en un navegador
    - Algunos feeds pueden requerir autenticación o tener restricciones de acceso

2. **El feed se carga pero no aparece contenido**:

    - El feed puede estar vacío o no estar publicando contenido actualmente
    - El formato del feed podría no ser compatible (intenta con un feed alternativo)
    - Intenta con un feed diferente y más activo

3. **El contenido aparece ilegible o formateado incorrectamente**:

    - Intenta con un modo de difuminado diferente
    - El feed podría contener caracteres especiales o formato que no es compatible
    - Considera usar un servicio de filtrado de feeds para limpiar el contenido

4. **El feed deja de actualizarse**:

    - El sitio web de origen puede haber cambiado la URL de su feed
    - Puede haber problemas temporales del servidor
    - Intenta eliminar y volver a agregar el feed

5. **La implementación falla**:

    - Asegúrate de que tu dispositivo esté conectado correctamente a SenseCraft HMI
    - Verifica la conexión a internet de tu dispositivo
    - Reinicia tu dispositivo e intenta implementar nuevamente

## Conclusión

La función RSS en SenseCraft HMI proporciona una manera poderosa de convertir tus dispositivos con pantalla en pantallas de información dinámicas. Al conectarte a feeds RSS, puedes crear pantallas que se actualizan automáticamente para noticias, clima, actualizaciones técnicas o cualquier otro contenido disponible a través de RSS.

Recuerda que la calidad de tu pantalla RSS depende en gran medida de los feeds que elijas. Experimenta con diferentes feeds, intervalos de actualización y configuraciones de visualización para crear la pantalla de información perfecta para tus necesidades.

