# 📱 Sistema de recordatorios - WhatsApp

Sistema completo para envío masivo de recordatorios de webinar a través de WhatsApp, compuesto por dos herramientas integradas, todo desde un único archivo HTML.


## 🎯 Descripción general

Este sistema está contenido en **un único archivo HTML** (`index.html`), que incluye dos herramientas integradas en una sola interfaz:

1. **📊 Generador de plantilla excel**  
   Crea un archivo Excel estructurado con 3 hojas y fórmulas automatizadas.
   
2. **📱 Envío de mensajes por WhatsApp**  
   Automatiza el envío personalizado de recordatorios utilizando los datos del Excel.

## 🚀 Características principales

### 📊 Generador de excel
- ✅ **Generación automática** de estructura Excel con 3 hojas
- ✅ **Configuración personalizada** de fecha, hora, nombre y URL del webinar
- ✅ **Fórmulas automáticas** para NOMBRE COMPLETO y TELEFONO FORMATEADO
- ✅ **Plantillas de mensajes** predefinidas incluidas
- ✅ **Escalable hasta 1000+ participantes**

### 📱 Automatizador de mensajes
- ✅ **Carga del archivo Excel** generado
- ✅ **Personalización de mensajes** con etiquetas dinámicas
- ✅ **Vista previa** del mensaje antes del envío
- ✅ **Envío masivo controlado** a través de WhatsApp Web
- ✅ **Seguimiento** del progreso de envío en tiempo real
- ✅ **Gestión de mensajes** guardados para reutilización

## 📋 Flujo de trabajo completo

### 🔧 Paso 1: Generar el excel base
1. Abre `whatsapp-webinar-generador.html` en tu navegador
2. Configura los datos del webinar:
   - **📅 Fecha:** Fecha del webinar
   - **🕐 Hora:** Hora del webinar (ej: 20:00)
   - **🎯 Nombre:** Nombre del webinar
   - **🌐 URL:** Enlace del webinar
   - **👥 Filas:** Cantidad de participantes (10-1000)
3. Haz clic en **"📄 Generar Excel Plantilla"**
4. Se descarga automáticamente el archivo Excel estructurado

### 📝 Paso 2: Completar los datos
1. Abre el archivo Excel generado
2. Ve a la hoja **"Identificacion"**
3. Completa los datos de tus participantes:
   - **NOMBRE:** Nombre del participante
   - **APELLIDOS:** Apellidos del participante  
   - **TELEFONO:** Número de teléfono (9 dígitos)
4. **¡Las demás columnas se completan automáticamente!**
   - La hoja **"Datos"** se rellena con fórmulas automáticas
   - **NOMBRE COMPLETO** = NOMBRE + APELLIDOS
   - **TELEFONO FORMATEADO** = añade "34" si es necesario

### 📱 Paso 3: Enviar mensajes masivos
1. Abre `whatsapp-webinar-auto.html` en tu navegador
2. Haz clic en **"Archivo Excel"** y selecciona tu archivo completado
3. Haz clic en **"📖 Analizar datos"**
4. Revisa las estadísticas cargadas
5. Personaliza tu mensaje:
   - Selecciona un **tipo de mensaje** predefinido
   - O crea tu **mensaje personalizado**
   - Usa las **etiquetas disponibles** para personalizar
6. Haz clic en **"👀 Vista previa"** para revisar el mensaje
7. Haz clic en **"🚀 Iniciar envío masivo"**
8. Confirma cada envío haciendo clic en **"📤 Enviar siguiente"**

## 📊 Estructura del excel generado

### Hoja "Identificacion" (Para completar manualmente)
```
NOMBRE     | APELLIDOS    | TELEFONO
Juan       | Pérez        | 612345678
María      | García       | 623456789
Carlos     | López        | 634567890
```

### Hoja "Datos" (Se completa automáticamente)
```
FECHA    | HORA  | NOMBRE WEBINAR           | URL                    | NOMBRE COMPLETO | TELEFONO FORMATEADO
26/6/25  | 20:00 | WEBINAR MARKETING DIGITAL| https://meet.com/...   | Juan Pérez      | 34612345678
26/6/25  | 20:00 | WEBINAR MARKETING DIGITAL| https://meet.com/...   | María García    | 34623456789
```

### Hoja "Mensajes" (Con plantillas predefinidas)
```
Identificador              | Mensaje
Recordatorio Webinar       | ¡Hola {Nombre}! Te recordamos...
Confirmación Asistencia    | ¿Confirmas tu asistencia...
Recordatorio Urgente       | 🚨 ¡RECORDATORIO URGENTE!...
```

## 🏷️ Etiquetas disponibles

Usa estas etiquetas en tus mensajes para personalización automática:

| Etiqueta | Descripción | Ejemplo |
|----------|-------------|---------|
| `{Nombre}` | Nombre del participante | Juan |
| `{Apellidos}` | Apellidos del participante | Pérez García |
| `{FECHA}` | Fecha del webinar | 26/6/25 |
| `{HORA}` | Hora del webinar | 20:00 |
| `{NOMBRE WEBINAR}` | Nombre del webinar | WEBINAR DE MARKETING |
| `{URL}` | Enlace del webinar | https://meet.com/... |
| `{NOMBRE COMPLETO}` | Nombre + Apellidos | Juan Pérez García |
| `{TELEFONO FORMATEADO}` | Teléfono con prefijo | 34612345678 |

## 💬 Ejemplo de mensaje personalizado

```
¡Hola {Nombre}! 👋

Te recordamos que tienes programado el webinar:
📅 *{NOMBRE WEBINAR}*
🗓️ Fecha: {FECHA}
🕐 Hora: {HORA}

🌐 Accede aquí: {URL}

¡No te lo pierdas! 🚀

¿Tienes alguna duda? ¡Escríbenos!
```

**Resultado para Juan Pérez:**
```
¡Hola Juan! 👋

Te recordamos que tienes programado el webinar:
📅 *WEBINAR DE MARKETING DIGITAL*
🗓️ Fecha: 26/6/25
🕐 Hora: 20:00

🌐 Accede aquí: https://teams.microsoft.com/meet/123456

¡No te lo pierdas! 🚀

¿Tienes alguna duda? ¡Escríbenos!
```

## ⚠️ Requisitos y consideraciones

### 📋 Antes de empezar
- **WhatsApp Web** debe estar abierto y conectado
- **Navegador moderno** (Chrome, Firefox, Safari, Edge)
- **Archivo Excel** generado con la herramienta incluida

### 📱 Formato de teléfonos
- **Formato español:** 9 dígitos (ej: 612345678)
- **Se acepta:** 612345678, +34612345678, 34612345678
- **El sistema añade automáticamente** el prefijo +34 si no está presente

### 🚨 Límites de WhatsApp
- **Envío controlado:** Un mensaje por vez para evitar bloqueos
- **Confirmación manual:** Cada mensaje se abre en WhatsApp Web para confirmar
- **Respeta los límites** de WhatsApp para evitar restricciones

## 🔧 Solución de problemas

### ❌ Error al generar Excel
- Verifica que hayas introducido una **fecha válida**
- Asegúrate de que todos los campos obligatorios estén completos
- Prueba con un número menor de filas primero

### ❌ Error al cargar Excel en el automatizador
- Verifica que el archivo tenga las hojas **"Identificacion"** y **"Datos"**
- Asegúrate de que hayas completado los datos en la hoja "Identificacion"
- Comprueba que los teléfonos tengan el formato correcto (9 dígitos)

### ❌ Mensajes no se envían
- Verifica que **WhatsApp Web** esté abierto y conectado
- Asegúrate de **confirmar cada envío** en la pestaña que se abre
- Revisa que los teléfonos sean válidos y estén activos en WhatsApp

### ❌ Etiquetas no se reemplazan
- Verifica que uses la **sintaxis correcta**: `{NOMBRE}` no `[NOMBRE]`
- Asegúrate de que el Excel tenga los **datos correctos** en la hoja "Datos"
- Revisa que hayas **cargado correctamente** el archivo

## 📞 Características avanzadas

### 💾 Gestión de mensajes
- **Guardar mensajes** personalizados para reutilización
- **Cargar mensajes** guardados desde el Excel
- **Plantillas predefinidas** listas para usar

### 📊 Seguimiento de envíos
- **Progreso en tiempo real** del envío masivo
- **Lista detallada** de participantes y estados
- **Registro de actividad** completo con timestamps

### 🎯 Personalización avanzada
- **Mensajes por tipo** (recordatorio, confirmación, urgente)
- **Vista previa** antes del envío
- **Edición en tiempo real** de mensajes

---

## 🎉 ¡Listo para usar!

Con este sistema tienes todo lo necesario para:
1. **Generar** archivos Excel estructurados para webinars
2. **Personalizar** mensajes con datos automáticos
3. **Enviar** recordatorios masivos de forma controlada
4. **Gestionar** listas de participantes eficientemente

**¡Perfecto para webinars, eventos, cursos online y cualquier convocatoria masiva!** 🚀
