---
title: Actualización y flasheo de firmware
description: Guía completa para actualizar y flashear firmware en tus dispositivos de pantalla e-paper
---

Antes de usar SenseCraft HMI, es altamente recomendable actualizar el firmware de tu dispositivo a la última versión. Esto asegura un rendimiento óptimo, corrección de errores y acceso a las últimas funciones.

## Aviso importante

Esta guía se centra en actualizar el firmware de SenseCraft HMI para su uso con la plataforma SenseCraft HMI. Mantener tu firmware actualizado garantiza que tengas acceso a las últimas características, mejoras y correcciones de errores.

## Herramienta Firmware Flasher

El Firmware Flasher es una herramienta esencial para mantener el software de tu dispositivo actualizado. Proporciona una interfaz simple, paso a paso, para flashear el firmware de SenseCraft HMI directamente desde tu navegador web.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_46.png" style={{width:400, height:'auto'}}/></div>

## Guía de flasheo paso a paso

### Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Cable USB**: Conecta tu dispositivo a tu computadora
- **Internet estable**: Para descargar archivos de firmware
- **Navegador moderno**: Se recomienda Chrome, Firefox, Safari o Edge
- **Energía del dispositivo**: Asegúrate de que tu dispositivo tenga suficiente energía

### Paso 1: Acceder al Firmware Flasher

1. Inicia sesión en tu cuenta de SenseCraft HMI
2. Navega a la pestaña **Espacio de trabajo**
3. Haz clic en el botón **Device Flasher** junto a tu dispositivo

### Paso 2: Seleccionar tu dispositivo

Antes de comenzar, asegúrate de que tu dispositivo esté conectado a tu computadora a través de un cable USB.

1. Haz clic en el botón **Seleccionar**
2. Aparecerá un modal pidiéndote que elijas tu dispositivo de una lista de hardware compatible

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_47.png" style={{width:400, height:'auto'}}/></div>

:::note
Si seleccionas el **ePaper DIY Kit - EE04**, se te solicitará un paso adicional: debes seleccionar el tipo y tamaño de pantalla específicos que estás usando con el kit. Esto asegura que los controladores de pantalla correctos estén incluidos en el firmware.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_48.png" style={{width:400, height:'auto'}}/></div>
:::

### Paso 3: Seleccionar firmware

Una vez que se selecciona un dispositivo, las opciones de firmware estarán disponibles.

1. Haz clic en el menú desplegable bajo **Seleccionar firmware** para ver una lista de versiones de firmware de SenseCraft HMI disponibles para tu dispositivo
2. Elige la versión que deseas instalar:
   - **Última versión** (Recomendado para el mejor rendimiento y las últimas funciones)
   - **Versiones anteriores** (si es necesario para requisitos de compatibilidad específicos)

**Opciones adicionales:**
- **Conectar monitor serial**: Este botón abre un monitor serial en tu navegador, que es una herramienta avanzada para ver mensajes de depuración y registros del dispositivo durante el proceso de flasheo

### Paso 4: Flashear el firmware

Este es el paso final donde el firmware se escribe en el dispositivo.

1. Haz clic en el botón **Flash** para comenzar el proceso
2. **Importante**: No desconectes el dispositivo ni cierres la pestaña del navegador hasta que el proceso esté completo
3. La herramienta mostrará una barra de progreso indicando el estado del flasheo

:::tip
Verás una casilla de verificación etiquetada **Full Flash**. Ten mucho cuidado con esta opción:

**Flash estándar (sin marcar)**:
- Actualiza el firmware pero conserva tu configuración guardada
- Mantiene las credenciales de Wi-Fi y la configuración del dispositivo
- Recomendado para actualizaciones regulares

**Full Flash (marcado)**:
- Borra **toda** la memoria flash del dispositivo
- **Esto eliminará toda la configuración guardada, incluida tu contraseña de Wi-Fi**
- Necesitarás reconfigurar tu conexión Wi-Fi después de un Full Flash
- Recomendado para solucionar problemas, realizar un "restablecimiento de fábrica" o cuando experimentes problemas persistentes
:::

## Después del flasheo

### Primer arranque
1. Espera a que el dispositivo se reinicie automáticamente
2. El dispositivo arrancará con el nuevo firmware
3. Verifica la pantalla del dispositivo para ver si hay mensajes de error

### Próximos pasos - Configuración del dispositivo

Después de flashear exitosamente el firmware de SenseCraft HMI, necesitarás configurar tu dispositivo para el primer uso. Sigue las guías específicas del dispositivo a continuación:

**Para reTerminal E1001:**
- Guía de configuración completa: [Comenzando con reTerminal E1001 - Configuración de red](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1001/#network-setup)

**Para reTerminal E1002:**
- Guía de configuración completa: [Comenzando con reTerminal E1002 - Configuración de red](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/#network-setup)

Estas guías te guiarán a través de:
- Encender tu dispositivo
- Conectar a Wi-Fi
- Emparejar con la plataforma SenseCraft HMI
- Crear tu primer panel de control

### Reconfiguración (si se usó Full Flash)
Si realizaste un Full Flash, necesitarás:
1. **Reconectar a Wi-Fi**: Configura tu conexión de red nuevamente
2. **Reconectar a la plataforma**: Vuelve a agregar el dispositivo a tu cuenta de SenseCraft HMI
3. **Restaurar configuración**: Reconfigura cualquier ajuste personalizado

## Solución de problemas

### Problemas comunes

**Dispositivo no detectado**
- Asegúrate de que el cable USB esté conectado correctamente
- Intenta con un puerto USB diferente
- Verifica si los controladores del dispositivo están instalados
- Reinicia tu navegador

**Flasheo fallido**
- No desconectes el dispositivo durante el flasheo
- Asegúrate de tener una conexión a internet estable
- Intenta usar un navegador diferente
- Verifica el nivel de energía del dispositivo

**El dispositivo no arranca después del flasheo**
- Espera unos minutos para que el dispositivo se inicialice
- Intenta un Full Flash si usaste Flash estándar
- Revisa el monitor serial para ver mensajes de error
- Contacta al soporte si los problemas persisten

**Conexión Wi-Fi perdida**
- Esto es normal después de un Full Flash
- Reconfigura la configuración de Wi-Fi en el dispositivo
- Vuelve a agregar el dispositivo a tu cuenta de plataforma

### Obtener ayuda

- **Monitor serial**: Usa el monitor serial integrado para ver información de depuración
- **Documentación**: Consulta otras guías para problemas específicos
- **Foro de la comunidad**: [Foro de Seeed Studio](https://forum.seeedstudio.com/)
- **Soporte**: Contacta al soporte técnico (techsupport@seeed.io)


## Mejores prácticas

### Antes del flasheo
- **Hacer copia de seguridad de la configuración**: Anota la configuración importante del dispositivo
- **Entorno estable**: Asegúrate de tener energía e internet estables
- **Cerrar otras aplicaciones**: Libera recursos del sistema

### Durante el flasheo
- **No interrumpir**: Nunca desconectes ni cierres el navegador durante el flasheo
- **Monitorear el progreso**: Observa la barra de progreso y cualquier mensaje de estado
- **Ser paciente**: El flasheo puede tomar varios minutos

### Después del flasheo
- **Probar funcionalidad**: Verifica que todas las funciones funcionen correctamente
- **Actualizar plataforma**: Asegúrate de estar usando la última versión de la plataforma
- **Documentar cambios**: Lleva un registro de las versiones de firmware para solucionar problemas

---

*¿Listo para comenzar a usar tu dispositivo actualizado? Consulta nuestra [Guía de interfaz del espacio de trabajo](/guides/workspace-interface/) para aprender cómo crear tu primer proyecto.*

