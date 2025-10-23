---
title: Implementación en tu dispositivo
description: Guía completa para implementar tus proyectos de SenseCraft HMI en tus dispositivos de pantalla e-paper
---

Una vez que hayas creado tu contenido usando cualquiera de las funciones de SenseCraft HMI (Panel de control, Galería, Canvas, RSS o Web), querrás implementarlo en tu dispositivo Seeed. Esta guía cubre el proceso de implementación para todos los tipos de contenido.

## Vista previa antes de la implementación

Antes de implementar tu contenido en el dispositivo, es importante obtener una vista previa de cómo se verá:

Paso 1. Haz clic en el botón "Vista previa" en la barra de herramientas superior

Paso 2. Revisa cómo aparecerá tu diseño en el dispositivo

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_24.png" style={{width:400, height:'auto'}}/></div>

Paso 3. Realiza los ajustes necesarios a tu diseño

:::tip
La función de vista previa te permite ver exactamente cómo aparecerá tu contenido en la pantalla del dispositivo, ayudándote a identificar cualquier problema de diseño antes de la implementación.
:::

## Guardar tu diseño

Antes de implementar, asegúrate de guardar tu trabajo:

Paso 1. Haz clic en el botón "Guardar" para almacenar tu diseño actual

Paso 2. Tu diseño se guardará en la nube de SenseCraft HMI

:::note
Guardar tu diseño garantiza que tu trabajo se conserve y se pueda acceder desde cualquier dispositivo o navegador.
:::

## Implementar en el dispositivo

Una vez que estés satisfecho con tu vista previa y hayas guardado tu diseño:

Paso 1. Asegúrate de que tu dispositivo esté conectado y muestre el estado "En línea"

Paso 2. Haz clic en el botón "Implementar"

Paso 3. Espera a que el proceso de implementación se complete

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_25.png" style={{width:400, height:'auto'}}/></div>

Paso 4. Tu diseño aparecerá en tu dispositivo conectado

## Consideraciones de implementación

Para una implementación exitosa en dispositivos Seeed, considera lo siguiente:

### 1. Compatibilidad del dispositivo
- Asegúrate de que tu diseño esté optimizado para la resolución de pantalla específica de tu dispositivo
- Los diferentes dispositivos tienen diferentes tamaños de pantalla y capacidades
- Prueba tu diseño en la resolución del dispositivo objetivo

### 2. Estado de conexión
- Asegúrate de que tu dispositivo muestre el estado "En línea" antes de implementar
- Verifica que tu dispositivo esté conectado correctamente a internet
- Verifica que el dispositivo esté emparejado con tu cuenta de SenseCraft HMI

### 3. Componentes de datos
- Si usas componentes de datos (Clima, Acciones, etc.), asegúrate de que tu dispositivo tenga conectividad a internet
- Algunas fuentes de datos pueden requerir claves API o autenticación
- Verifica que todas las fuentes de datos externas sean accesibles

### 4. Sensores del dispositivo
- Componentes como Batería, Temperatura y Humedad solo funcionarán con dispositivos compatibles de la serie reTerminal E de Seeed con pantalla ePaper que tengan los sensores apropiados
- Verifica que tu dispositivo tenga el hardware requerido para los componentes basados en sensores

### 5. Tasa de actualización
- Establece un tiempo de intervalo apropiado según la frecuencia con la que tus datos necesitan actualizarse y las capacidades de tu dispositivo
- Considera la duración de la batería al establecer intervalos de actualización
- Equilibra entre frescura de datos y consumo de energía

---

**¡Felicidades!** Has implementado exitosamente tu contenido en tu dispositivo. Tu pantalla e-paper ahora debería mostrar tu diseño personalizado.

*¿Necesitas ayuda con funciones específicas? Consulta nuestras guías detalladas para las funciones [Interfaz del espacio de trabajo](/guides/workspace-interface/), [Galería](/guides/sensecraft-hmi-gallery/), [Canvas](/guides/sensecraft-hmi-canvas/), [RSS](/guides/sensecraft-hmi-rss/) y [Web](/guides/sensecraft-hmi-web/).*

