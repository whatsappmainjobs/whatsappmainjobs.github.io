# 📱 Sistema de Recordatorios de Webinar - WhatsApp

Sistema simplificado para envío masivo de recordatorios de webinar a través de WhatsApp.

## 🚀 Características

- ✅ **Carga de archivo Excel** con datos de participantes
- ✅ **Personalización de mensajes** con etiquetas dinámicas
- ✅ **Vista previa** del mensaje antes del envío
- ✅ **Envío masivo** automático a través de WhatsApp Web
- ✅ **Seguimiento** del progreso de envío
- ✅ **Registro de actividad** en tiempo real

## 📋 Requisitos del archivo Excel

Tu archivo Excel debe contener las siguientes columnas:

| Columna | Descripción | Obligatorio |
|---------|-------------|-------------|
| **Nombre** | Nombre del participante | ✅ Sí |
| **Apellidos** | Apellidos del participante | ❌ No |
| **Teléfono** | Número de teléfono (con o sin +34) | ✅ Sí |
| **URL** | Enlace del webinar | ❌ No |
| **Fecha** | Fecha y hora del webinar | ❌ No |

### 📊 Formato de ejemplo:

```
Nombre    | Apellidos | Teléfono   | URL                                    | Fecha
Juan      | Pérez     | 612345678  | https://meet.google.com/abc-defg-hij   | 2024-01-15 18:00
María     | García    | 623456789  | https://meet.google.com/abc-defg-hij   | 2024-01-15 18:00
```

## 🎯 Etiquetas disponibles

Puedes usar estas etiquetas en tu mensaje para personalizarlo:

- `{Nombre}` - Nombre del participante
- `{Apellidos}` - Apellidos del participante  
- `{URL}` - Enlace del webinar
- `{Fecha}` - Fecha formateada del webinar
- `{Hora}` - Hora del webinar

### 💬 Ejemplo de mensaje:

```
Hola {Nombre}, 

Te recordamos que mañana tienes el webinar programado.

📅 Fecha: {Fecha}
🕐 Hora: {Hora}
🔗 Enlace: {URL}

¡Nos vemos allí!

Saludos,
Tu equipo
```

## 📱 Cómo usar

### 1. Preparar el archivo Excel
- Crea un archivo Excel con las columnas mencionadas
- Asegúrate de que los teléfonos estén en formato español (9 dígitos)
- Guarda el archivo como `.xlsx`

### 2. Cargar datos
- Abre el archivo HTML en tu navegador
- Haz clic en "Seleccionar archivo" y elige tu Excel
- Haz clic en "📖 Analizar datos"

### 3. Crear el mensaje
- Escribe tu mensaje personalizado usando las etiquetas disponibles
- Haz clic en "👀 Vista previa" para ver cómo se verá
- Ajusta el mensaje si es necesario

### 4. Iniciar envío
- Haz clic en "🚀 Iniciar envío masivo"
- Revisa la lista de participantes
- Haz clic en "📤 Enviar siguiente" para cada mensaje

## ⚠️ Importante

- **WhatsApp Web**: Debes tener WhatsApp Web abierto y conectado
- **Confirmación manual**: Cada mensaje se abre en una nueva pestaña para que confirmes el envío
- **Límites de WhatsApp**: Respeta los límites de envío de WhatsApp para evitar bloqueos
- **Teléfonos válidos**: Solo se procesan participantes con nombre y teléfono válido

## 🔧 Solución de problemas

### Error al cargar el archivo
- Verifica que el archivo sea `.xlsx`
- Asegúrate de que tenga al menos una fila de encabezados
- Comprueba que las columnas "Nombre" y "Teléfono" existan

### Teléfonos no válidos
- Los teléfonos deben tener 9 dígitos (formato español)
- Se aceptan formatos: 612345678, +34612345678, 34612345678

### Mensaje no se envía
- Verifica que WhatsApp Web esté abierto
- Comprueba que estés conectado a WhatsApp Web
- Asegúrate de confirmar el envío en cada pestaña

## 📞 Soporte

Si tienes problemas o necesitas ayuda, revisa:
1. El registro de actividad en la parte inferior
2. Que todos los requisitos estén cumplidos
3. Que el formato del archivo Excel sea correcto

---

**¡Listo para enviar recordatorios masivos de webinar! 🎉** 