# Core RO - Bot de Discord para Ragnarok Online

> [!WARNING]  
>Este github puede estar actualizado como puede que no esté actualizado. Mantente informado siempre en https://corero.zubkan.com

> [!IMPORTANT]
> **Este bot requiere obligatoriamente conexión a la base de datos MySQL de un servidor Ragnarok (rAthena)**. Sin la DB del juego, la mayoría de funcionalidades no operan.

[![Discord.py](https://img.shields.io/badge/Discord.py-2.3+-blue.svg)](https://github.com/Rapptz/discord.py)
[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://python.org)
[![MySQL](https://img.shields.io/badge/MySQL-rAthena%20Compatible-orange.svg)]()

**Core RO** es un bot de Discord diseñado específicamente para servidores de **Ragnarok Online** que utilizan emuladores como rAthena. Conecta directamente con la base de datos del juego para ofrecer integración completa entre Discord y el servidor RO.

## 📋 Tabla de Contenidos

- [🎯 ¿Para quién es este bot?](#-para-quién-es-este-bot)
- [⚡ Requisitos Obligatorios](#-requisitos-obligatorios)
- [🎮 Funcionalidades para Usuarios](#-funcionalidades-para-usuarios)
- [🏢 Funcionalidades para Dueños de Servidor](#-funcionalidades-para-dueños-de-servidor)
- [📊 Comandos Disponibles](#-comandos-disponibles)
- [⚙️ Sistemas Automáticos](#️-sistemas-automáticos)
- [⚠️ Advertencias y Consideraciones](#-advertencias-y-consideraciones)
- [💡 Tips y Mejores Prácticas](#-tips-y-mejores-prácticas)
- [❓ FAQ](https://discord.zubkan.com)

---

## 🎯 ¿Para quién es este bot?

### 👥 Para Jugadores de Ragnarok Online
- Verificación segura de cuenta Discord ↔ Personaje RO
- Consulta de información de personajes e ítems
- Sistema de niveles por participación en Discord
- Soporte via tickets integrado
- Notificaciones automáticas al conectar al juego

### 🏢 Para Dueños de Servidores RO
- **Integración nativa con rAthena** - No requiere APIs externas
- Sistema de limpieza automática de usuarios inactivos
- Tracking de invitaciones con estadísticas
- Eventos automáticos sincronizados con el juego
- Notificaciones de streamers de la comunidad
- Mensajes programados (broadcasts)

---

## ⚡ Requisitos Obligatorios

> [!CAUTION]
> **Este bot NO funcionará sin estos requisitos:**

| Requisito | Descripción |
|-----------|-------------|
| **Base de datos MySQL** | Conexión directa a la DB del servidor Ragnarok (rAthena/Hercules) |
| **Discord Key** | se otorga codigo para su funcionalida |
| **Python 3.11+** | Para ejecutar el bot |
| **Permisos de Admin** | En el servidor Discord (para expulsiones, gestión de canales) |

> [!WARNING]
> **Sin la base de datos del juego, estas funciones NO operan:**
> - Verificación de cuentas (`/verified`)
> - Búsqueda de personajes (`/find`)
> - Welcome Back al conectar al juego
> - Eventos automáticos del servidor
> - Estadísticas de jugadores

---

## 🎮 Funcionalidades para Usuarios

### 🔐 Verificación de Cuenta Discord ↔ RO

Vincula tu cuenta de Discord con tu personaje del juego.

**¿Cómo funciona?**
1. Obtén tu Discord Key del juego (Config > Discord Key)
2. Envíala en el canal de verificación (sin comandos)
3. ¡Listo! Recibes rol de verificado automáticamente

> [!TIP]
> **Beneficios de verificarte:**
> - Acceso completo al servidor Discord
> - Mensaje automático al conectar al juego
> - Soporte prioritario via tickets
> - Participación en sorteos exclusivos

---

### 📊 Sistema de Niveles Discord

Gana XP participando en la comunidad y sube de nivel.

| Acción | XP Ganado | Cooldown |
|--------|-----------|----------|
| Mensaje en chat | 80-150 XP | 5 segundos |

**Características:**
- 📈 Curva progresiva (niveles superiores requieren más XP)
- 🔔 Anuncios automáticos al subir de nivel
- 🏆 Leaderboard competitivo
- 👤 Opción `/nottagrank` para desactivar menciones

---

### 🔍 Búsqueda de Personajes (`/find`)

Consulta información pública de cualquier personaje del servidor.

**Búsqueda por:** ID del personaje o nombre exacto

**Datos mostrados:**
- 📊 Nivel base / Job
- 🏹 Clase y sprites
- 🗺️ Última ubicación conocida
- 🌍 País de origen
- ⏰ Tiempo de juego acumulado
- 💰 Zeny (opcional)
- 📅 Fecha de creación del personaje

---

### � Leaderboard (`/top`)

Tabla de clasificación de usuarios Discord por nivel.

**Incluye:**
- Posición en ranking
- Nivel actual y XP
- Mensajes totales
- Invitaciones realizadas

> [!NOTE]
> Usa los botones ⬅️ ➡️ para navegar entre páginas. Solo el autor del comando puede interactuar con los botones.

---

### 🎁 Sorteos (`/giveaway`)

Sistema completo de sorteos para la comunidad.

**Participación:**
- Botón "Join Giveaway 🎉" en mensaje del sorteo
- Múltiples ganadores posibles
- Contador regresivo visible
- Selección aleatoria automática al finalizar

---

### 🗳️ Votaciones (`/voting`)

Crea y participa en encuestas de la comunidad.

**Features:**
- Múltiples opciones configurables
- Resultados en tiempo real
- Tiempo límite programable
- Permite cambio de voto

---

### 🎫 Tickets de Soporte

Sistema de soporte categorizado con canales privados.

| Categoría | Uso |
|-----------|-----|
| ✅ Verificado | Problemas con verificación de cuenta |
| 🛠️ Soporte | Consultas técnicas o generales |
| 🚨 Reporte | Bugs, cheats, violaciones de reglas |
| 🛒 Tienda | Dudas sobre donaciones/compras |
| 📢 Apelación | Solicitar revisión de sanciones |

**Beneficios:**
- Canal privado temporal
- Backup del ticket enviado por DM al cerrar
- Panel interactivo para gestión

---

### � Información de Ítems (`/itemid`)

Consulta detalles de cualquier ítem del juego.

**Muestra:**
- Sprite del ítem
- Descripción completa
- Stats y atributos
- Información específica por tipo de ítem

---

### 🌐 Soporte Multi-idioma (`/lang`)

Cambia el idioma del bot.

- 🇺🇸 English
- 🇪🇸 Español

---

## 🏢 Funcionalidades para Dueños de Servidor

### 🧹 Limpieza Automática de Inactivos

Sistema automático que mantiene la comunidad activa.

**Timeline de inactividad:**

| Días | Acción |
|------|--------|
| 15 | 📩 Recordatorio por MD |
| 30 | 🚨 Última advertencia |
| 37 | ❌ Expulsión automática |

**¿Qué cuenta como actividad?**
- ✉️ Enviar mensajes
- 👍 Reaccionar a mensajes
- 🎙️ Entrar a canales de voz (aunque no hables)

> [!TIP]
> **Staff y roles especiales están protegidos** de la expulsión automática.

---

### 🤝 Tracking de Invitaciones

Rastreo automático de quién invitó a quién.

**Automático:**
- Detecta el invite link utilizado
- Mensaje de bienvenida mencionando al invitador
- Estadísticas de invitaciones por usuario
- Actualización en tiempo real

---

### 📺 Notificaciones de Streamers

Anuncios automáticos cuando streamers de la comunidad están en vivo.

**Plataformas:** YouTube, Twitch, Kick

**Comportamiento:**
- � Embed automático cuando están ONLINE
- � Eliminación automática cuando están OFFLINE
- Thumbnail de la plataforma
- Link directo al stream

---

### 📢 Broadcast Timer

Mensajes programados recurrentes.

**Configuración:**
- Intervalos personalizables (minutos)
- Embeds con título, descripción e imagen
- Canal destino configurable
- Activación/desactivación instantánea

---

## ⚙️ Sistemas Automáticos

### 🎮 Welcome Back

Mensaje privado automático al conectar al juego.

**Requiere:**
- Cuenta verificada (Discord Key vinculado)
- DMs abiertos

**Contenido:**
- Sprite del personaje según clase/sexo
- Última conexión registrada
- Mensaje personalizado de bienvenida

> [!NOTE]
> Se verifica cada 30 segundos. Solo se envía una vez por sesión de juego.

---

### � Eventos del Juego

Anuncios automáticos de eventos activos en el servidor RO.

**Sincronizado con:**
- Tabla de eventos de la base de datos
- Estado activo/inactivo
- Tiempo restante (si aplica)

---

## � Comandos Disponibles

### 🎮 Welcome Back (Bienvenida al Conectar)

Cuando te conectas al juego con una cuenta verificada:

- 📩 Recibes un mensaje privado en Discord automáticamente
- 🖼️ Muestra la imagen de tu personaje (según clase y sexo)
- ⏰ Información de tu última conexión
- 💬 Mensaje personalizado de bienvenida

**Funcionamiento:**
- Se activa cada 30 segundos verificando jugadores online
- Solo se envía una vez por sesión de juego
- Si tienes DMs desactivados, no recibirás el mensaje

---

### 🎉 Eventos Automáticos

Anuncios automáticos de eventos en el juego.

**Características:**
- 📢 Anuncios automáticos cuando un evento se activa
- 🔔 Notificación en canal designado
- ⏰ Información de tiempo restante
- 🔄 Estado del evento (activo/inactivo)

---

### 📺 Notificaciones de Streamers

Recibe notificaciones cuando streamers del servidor están en vivo.

**Plataformas soportadas:**
- YouTube
- Twitch
- Kick

**Características:**
- 🟢 Embed verde cuando el streamer está ONLINE
- 🔴 Eliminación automática cuando está OFFLINE
- 🔗 Link directo al stream
- 🖼️ Logo de la plataforma

---

### 🧹 Limpieza de Inactivos

Sistema para mantener la comunidad activa.

**Timeline:**
| Días sin actividad | Acción |
|-------------------|--------|
| 15 días | 📩 Recordatorio por mensaje privado |
| 30 días | 🚨 Última advertencia |
| 37 días | ❌ Expulsión automática |

**¿Qué cuenta como actividad?**
- ✉️ Enviar mensajes
- 👍 Reaccionar a mensajes
- 🎙️ Entrar a canales de voz

**Protecciones:**
- El contador se reinicia automáticamente al mostrar actividad
- Staff y roles especiales están protegidos
- Si regresas al servidor, el proceso se reinicia desde el día 0

---

### 🤝 Sistema de Invitaciones

Reconocimiento automático de quién invitó a quién.

**Características:**
- 🔗 Detecta automáticamente qué invite link se usó
- 📨 Mensaje de bienvenida mencionando al invitador
- 📊 Registro de invitaciones para estadísticas
- 🔄 Actualización automática del contador

---

### 📢 Broadcast Timer

Mensajes programados automáticos del servidor.

**Características:**
- ⏰ Intervalos configurables (ej: cada X minutos)
- 🎨 Embeds personalizados
- 📍 Canales designados
- 🖼️ Soporte para imágenes

---

## 📋 Información Adicional

### 🔒 Seguridad

- **Tu Discord Key es única** para tu cuenta
- **Solo puede usarse una vez** con una cuenta de Discord
- **Nunca compartas tu key** con nadie
- **El staff nunca pedirá tu key**

### 📞 Soporte

¿Necesitas ayuda?
- Crea un ticket en el canal de soporte
- Contacta al staff del servidor
- Revisa las reglas con `/rulesro` o `/rulesdc`

### 🌟 Comandos de Utilidad

| Comando | Descripción |
|---------|-------------|
| `/verified` | Verifica tu cuenta con Discord Key |
| `/find` | Busca personajes del juego |
| `/top` | Muestra ranking de niveles |
| `/rulesro` | Muestra reglas del servidor |
| `/rulesdc` | Muestra reglas de Discord |
| `/lang` | Cambia el idioma del bot |
| `/itemid` | Información de ítems |
| `/nottagrank` | Activa/desactiva menciones en subidas de nivel |

---

## 🏗️ Arquitectura y Tecnología

> [!IMPORTANT]
> Este bot está diseñado **exclusivamente** para funcionar con la **base de datos MySQL del servidor Ragnarok** (rAthena u otro emulador compatible). Sin conexión a la DB del servidor, el bot **NO puede funcionar**.

### 🔗 Integración Directa con el Servidor

El bot se conecta **directamente** a la base de datos MySQL del servidor de juego, permitiendo:
- 🎮 Lectura en tiempo real de personajes online
- 🔐 Verificación automática mediante Discord Key (almacenada en la DB del juego)
- 📊 Consulta de información de personajes, ítems, y estadísticas
- 🔔 Eventos automáticos sincronizados con el estado del servidor
- 🎉 Detección automática de jugadores verificados conectándose al juego

> [!CAUTION]
> **Sin conexión a la DB del servidor, el bot NO puede funcionar correctamente.**

### 🛠️ Stack Tecnológico
- **Python 3.11+**
- **discord.py** - Framework principal de Discord
- **aiomysql / PyMySQL** - Conexión asíncrona a MySQL

---

## ⚠️ Advertencias y Consideraciones

> [!CAUTION]
> **Dependencia de Base de Datos**
> No intentes usar el bot sin conexión a la DB del servidor. La mayoría de funciones dependen de la base de datos del juego para funcionar correctamente.

> [!WARNING]
> **Discord Key Sensible**
> Nunca compartas tu Discord Key con nadie. Es única, irrepetible y vinculada permanentemente a tu cuenta.

> [!WARNING]
> **Expulsión por Inactividad**
> Mantén actividad regular en el servidor Discord o serás expulsado automáticamente tras **37 días** sin interactuar.

> [!NOTE]
> **Cooldown de XP**
> Hay un cooldown de **5 segundos** entre mensajes para ganar XP. No intentes farmear enviando mensajes rápidos.

> [!NOTE]
> **DMs Cerrados**
> Si tienes los mensajes privados desactivados, no recibirás:
> - Mensajes de bienvenida al conectar al juego
> - Advertencias de inactividad
> - Backups de tickets cerrados

> [!TIP]
> **Reacciones cuentan como actividad**
> Reaccionar a mensajes y entrar a canales de voz (aunque no hables) también cuenta como actividad para evitar la expulsión por inactividad.

### � Seguridad

> [!IMPORTANT]
> El staff **NUNCA** pedirá tu Discord Key. Si alguien lo solicita, repórtalo inmediatamente.

- Los tickets son privados y solo accesibles por ti y el staff
- La verificación es irreversible (una vez vinculada, no se puede desvincular fácilmente)
- El bot solo lee información pública de personajes; datos sensibles están protegidos

---

## 💡 Tips y Mejores Prácticas

> [!TIP]
> **Verifícate lo antes posible**
> La verificación desbloquea todas las funcionalidades del bot incluyendo el mensaje de bienvenida al conectar al juego.

> [!TIP]
> **Desactiva menciones de nivel**
> Usa `/nottagrank` si no quieres ser mencionado en los anuncios de subida de nivel del canal.

> [!TIP]
> **Entra a canales de voz**
> Aunque no hables, entrar a canales de voz cuenta como actividad para evitar la expulsión por inactividad.

### 🛡️ Para Server Admins (Autohosteado)

> [!IMPORTANT]
> **Configuración MySQL requerida**
> Asegúrate de configurar correctamente las variables de entorno para la conexión MySQL y que la estructura de tablas del rAthena sea compatible.

> [!NOTE]
> **Permisos de Discord**
> El bot requiere permisos de administrador en Discord para algunas funciones avanzadas como expulsión de inactivos.

- Revisa los logs regularmente para detectar errores de conexión a la DB
- El sistema de niveles tiene fórmulas ajustadas; los primeros niveles son más accesibles
- Las invitaciones se rastrean automáticamente; no necesitas comandos extra
- Los eventos del juego se detectan automáticamente si la DB está correctamente configurada

---

## 🎨 Características Generales

- ✅ **Soporte bilingüe** (Español/English)
- ✅ **Sistema de tickets** organizado por categorías
- ✅ **Integración nativa con MySQL** del servidor Ragnarok (rAthena)
- ✅ **Sistema de niveles y XP** basado en actividad
- ✅ **Eventos automáticos** sincronizados con el juego vía base de datos
- ✅ **Notificaciones de streamers** en tiempo real
- ✅ **Sistema de verificación** segura con Discord Key (integrada con DB del juego)
- ✅ **Búsqueda de personajes** e ítems directo desde la base de datos del servidor

---

**¡Gracias por usar Core RO!** 🚀
