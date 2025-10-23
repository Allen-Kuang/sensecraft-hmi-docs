---
title: Función Web
description: Presenta el uso de Web, una función de la plataforma SenseCraft HMI.
---

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/88.jpg" style={{width:800, height:'auto'}}/></div>

## Introducción

La función Web en [SenseCraft HMI](https://sensecraft.seeed.cc/hmi) te permite mostrar contenido web directamente en tus dispositivos con pantalla. Esta poderosa función transforma tu dispositivo en una pantalla web dedicada, capaz de mostrar paneles de control, sistemas de monitoreo, documentación o cualquier contenido web que necesites. A diferencia de los navegadores tradicionales, la función Web de SenseCraft HMI está optimizada para pantallas integradas y dispositivos IoT, lo que la hace perfecta para crear quioscos de información, monitores de estado o interfaces web dedicadas.

Este tutorial te guiará en el uso de la función Web en SenseCraft HMI, cubriendo la configuración, vista previa e implementación de contenido web en tu dispositivo.

Este artículo utilizará el [reTerminal E1002](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/) como ejemplo para explicar cómo usar esta función en la plataforma SenseCraft HMI.

## Primeros pasos con la función Web

### Acceder a la función Web

Paso 1. Navega a la plataforma SenseCraft HMI a continuación.<br>
[SenseCraft HMI](https://sensecraft.seeed.cc/hmi)<br>
Paso 2. Conecta tu dispositivo o selecciona un dispositivo ya emparejado para usar.<br>
Paso 3. Haz clic en **Contenido Web** en la barra lateral izquierda<br>

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/web_start_1.png" style={{width:1000, height:'auto'}}/></div>

paso 4. Ingresa una URL de página web, por ejemplo

```url
https://www.windy.com/
```

### Comprender la interfaz Web

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/web_start_2.png" style={{width:1000, height:'auto'}}/></div>

La interfaz Web consta de tres secciones principales:

1. **Panel de configuración de URL**: Ubicado en la parte superior, donde puedes ingresar direcciones web
2. **Área de visualización**: La sección principal donde se mostrará el contenido web después de la vista previa o implementación
3. **Botones de control**: Ubicados en la parte superior, incluidas las opciones de Vista previa, Guardar e Implementar

Al acceder por primera vez a la función Web, el área de visualización estará vacía hasta que configures y previsualices una página web.

## Configurar contenido web

### Agregar una página web

Paso 1. Localiza el panel de Configuración Web en la parte superior de la pantalla<br>
Paso 2. Encuentra el campo de entrada **URL**<br>
Paso 3. Ingresa una dirección web válida en el campo (por ejemplo, https://www.windy.com/)<br>

:::tip
Asegúrate de incluir la URL completa incluyendo el prefijo https:// o http://.
:::

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/web_configurate_1.png" style={{width:1000, height:'auto'}}/></div>

Paso 4. Haz clic en el botón **Establecer** para validar la URL

### Vista previa del contenido web

A diferencia de otras funciones en SenseCraft HMI, la función Web requiere un paso de vista previa explícito para mostrar el contenido:

Paso 1. Después de ingresar y establecer una URL, haz clic en el botón **Vista previa** en la barra de herramientas superior

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/web_configurate_2.png" style={{width:1000, height:'auto'}}/></div>

Paso 2. Espera a que la página web se cargue en el área de visualización<br>
Paso 3. Verifica si el contenido web se muestra correctamente y es apropiado para el tamaño de pantalla de tu dispositivo

:::note
El paso de vista previa es crucial ya que te permite verificar que el contenido web se mostrará correctamente en tu dispositivo antes de la implementación.
:::

### Guardar e implementar contenido web

Una vez que hayas previsualizado y confirmado que el contenido web se ve bien:

Paso 1. Haz clic en el botón **Guardar** para almacenar tu configuración web<br>
Paso 2. Haz clic en **Implementar** para enviar la configuración a tu dispositivo conectado<br>
Paso 3. Espera el mensaje de confirmación de implementación<br>

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/img/web_configurate_3.png" style={{width:1000, height:'auto'}}/></div>

Después de una implementación exitosa, tu dispositivo mostrará la página web configurada.

## Optimizar contenido web para dispositivos

No todos los sitios web están diseñados para pantallas pequeñas o dispositivos integrados. Aquí hay consejos para seleccionar y optimizar contenido web:

### Seleccionar contenido web amigable

1. **Elige sitios web responsivos para móviles**:

    - Los sitios diseñados para dispositivos móviles generalmente se mostrarán mejor en pantallas más pequeñas
    - Busca sitios con diseños adaptativos que funcionen bien en la resolución de tu dispositivo

2. **Considera páginas simples y ligeras**:

    - Los sitios web complejos con JavaScript pesado pueden cargarse lentamente o consumir más recursos
    - Las páginas estáticas generalmente funcionan mejor que las aplicaciones web dinámicas

3. **Evita sitios que requieran autenticación**:

    - Las sesiones de inicio de sesión pueden caducar, requiriendo intervención manual
    - Algunos métodos de autenticación pueden no funcionar bien en dispositivos integrados

### Tipos de contenido web recomendados

Aquí hay algunos tipos de contenido web que funcionan particularmente bien con la función Web de SenseCraft HMI:

1. **Paneles de control del clima**:

    - [Weather.gov](https://weather.gov)<br>
    - [Windy.com](https://www.windy.com/)<br>
    - [AccuWeather](https://www.accuweather.com/)<br>

2. **Paneles de control de monitoreo**:

    - Paneles de Grafana<br>
    - Paneles de control de automatización del hogar<br>
    - Páginas de estado del sistema<br>

3. **Pantallas de información**:

    - Horarios de tránsito<br>
    - Información de vuelos<br>
    - Disponibilidad de salas de reuniones<br>

4. **Documentación o referencia**:

    - Wikis locales<br>
    - Guías de procedimientos<br>
    - Información de referencia rápida<br>

## Crear contenido web personalizado

Para la mejor experiencia, considera crear páginas web personalizadas diseñadas específicamente para la pantalla de tu dispositivo:

### Páginas HTML simples

Puedes crear páginas HTML básicas optimizadas para la resolución de tu dispositivo. Aquí hay un ejemplo simple:

```html
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Panel de dispositivo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            font-size: 18px;
        }
        .container {
            padding: 15px;
        }
        .title {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 15px;
        }
        .info-box {
            border: 1px solid #ccc;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title">Estado del dispositivo</div>
        <div class="info-box">Temperatura: 22.5°C</div>
        <div class="info-box">Humedad: 45%</div>
        <div class="info-box">Batería: 87%</div>
    </div>
</body>
</html>
```

### Opciones de alojamiento para páginas personalizadas

Para mostrar contenido web personalizado, necesitarás alojarlo en algún lugar accesible para tu dispositivo:

1. **Servidor de red local**:

    - Configura un servidor web simple en tu red local
    - Usa herramientas como XAMPP, NGINX o un Raspberry Pi ejecutando un servidor web

2. **Servicios de alojamiento estático gratuitos**:

    - [GitHub Pages](https://pages.github.com/)
    - [Netlify](https://www.netlify.com/)
    - [Vercel](https://vercel.com/)

3. **Servicios en la nube con niveles gratuitos**:

    - [Firebase Hosting](https://firebase.google.com/products/hosting)
    - [AWS S3 Static Website Hosting](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)

## Casos de uso especiales

### Mostrar recursos de red local

La función Web se puede usar para mostrar recursos en tu red local:

1. **Paneles de control de automatización del hogar**:

    - Home Assistant: `http://homeassistant.local:8123`
    - OpenHAB: `http://openhab.local:8080`

2. **Herramientas de monitoreo de red**:

    - Paneles de administración de enrutadores
    - Paneles de control de monitoreo de red

3. **Servidores de medios locales**:

    - Página de estado de Plex
    - Interfaces web de NAS

:::tip
Por razones de seguridad, ten cuidado al mostrar interfaces administrativas en dispositivos públicamente visibles.
:::

### Rotación automática de páginas

Si deseas mostrar múltiples páginas web en rotación:

1. Crea una página HTML simple con JavaScript para recorrer las URLs:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Rotador de páginas</title>
    <style>
        body, html, iframe {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
            border: none;
            overflow: hidden;
        }
    </style>
    <script>
        // Array de URLs para rotar
        const urls = [
            'https://weather.gov',
            'https://example.com/dashboard',
            'https://example.com/calendar'
        ];
        
        let currentIndex = 0;
        
        function rotatePages() {
            document.getElementById('display-frame').src = urls[currentIndex];
            currentIndex = (currentIndex + 1) % urls.length;
            setTimeout(rotatePages, 30000); // Cambiar página cada 30 segundos
        }
        
        window.onload = rotatePages;
    </script>
</head>
<body>
    <iframe id="display-frame" src="about:blank"></iframe>
</body>
</html>
```

2. Aloja esta página usando uno de los métodos mencionados anteriormente

3. Ingresa la URL de esta página rotadora en la función Web de SenseCraft HMI

## Solución de problemas

### Problemas comunes de visualización web y soluciones

1. **La página web no se carga**:

    - Verifica que la URL sea correcta e incluya el prefijo http:// o https://. A veces obviamente ingresaste la URL correcta, pero aún no puedes obtener una vista previa, puedes intentar agregar "/" al final de la URL, puede haber un efecto milagroso.
    - Verifica si la página es accesible probando en un navegador regular
    - Asegúrate de que tu dispositivo tenga conectividad a internet
    - Algunos sitios web pueden bloquear la incrustación o tener restricciones de seguridad

2. **El contenido se muestra incorrectamente**:

    - Es posible que el sitio web no esté optimizado para el tamaño de pantalla de tu dispositivo
    - Intenta con una versión específica para móviles del sitio si está disponible
    - Considera crear una página personalizada específicamente para las dimensiones de tu pantalla

3. **Problemas de rendimiento**:

    - Los sitios web complejos con animaciones o JavaScript pesado pueden ejecutarse lentamente
    - Prueba páginas más simples o alternativas creadas personalizadas
    - Algunos sitios web pueden usar más memoria de la que tu dispositivo puede manejar

4. **La implementación falla**:

    - Asegúrate de que tu dispositivo esté conectado correctamente a SenseCraft HMI
    - Verifica la conexión a internet de tu dispositivo
    - Reinicia tu dispositivo e intenta implementar nuevamente

5. **El contenido necesita actualización frecuente**:

    - Algún contenido dinámico puede no actualizarse automáticamente
    - Considera establecer un intervalo de actualización en una página personalizada, o
    - Reimplementa periódicamente la configuración

## Mejores prácticas

### Consideraciones de seguridad

Al usar la función Web, ten en cuenta estas consideraciones de seguridad:

1. **Evita información sensible**:

    - No muestres páginas que contengan información personal o confidencial en dispositivos públicamente visibles
    - Ten cuidado con paneles de administración o interfaces de control

2. **Usa HTTPS cuando sea posible**:

    - Prefiere URLs seguras (https://) sobre no seguras (http://)
    - Esto ayuda a proteger los datos transmitidos a tu dispositivo

3. **Considera el aislamiento de red**:

    - Para pantallas que muestran recursos internos, considera usar una red separada
    - Usa reglas de firewall para limitar a qué puede acceder tu dispositivo

### Consejos de mantenimiento

Para mantener tus pantallas web funcionando sin problemas:

1. **Verificaciones periódicas**:

    - Verifica regularmente que el contenido mostrado aún funcione correctamente
    - Los sitios web pueden cambiar sus diseños o URLs sin previo aviso

2. **Actualizar marcadores**:

    - Mantén una lista de URLs útiles para tus pantallas
    - Prueba alternativas en caso de que tus sitios preferidos cambien

3. **Crear copias de seguridad**:

    - Para pantallas críticas, crea y aloja páginas de respaldo que se puedan implementar rápidamente
    - Esto garantiza la continuidad si un recurso web principal no está disponible

## Conclusión

La función Web en SenseCraft HMI proporciona una manera flexible de mostrar contenido web en tus dispositivos con pantalla. Siguiendo esta guía, puedes configurar, previsualizar e implementar páginas web para crear pantallas de información, paneles de control o pantallas de referencia adaptadas a tus necesidades.

Recuerda que no todo el contenido web es adecuado para pantallas pequeñas o dispositivos integrados. Para la mejor experiencia, considera usar sitios web responsivos para móviles o crear páginas web personalizadas diseñadas específicamente para las dimensiones y capacidades de tu dispositivo.

