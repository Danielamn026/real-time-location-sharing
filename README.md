# 	RealTimeLocationSharing

Aplicación Android para gestionar la disponibilidad de usuarios en tiempo real mediante geolocalización, autenticación con Firebase y un mapa interactivo basado en OpenStreetMap.

## Descripción

Taller03 es una app móvil diseñada para ayudar a los usuarios a:

- Registrarse e iniciar sesión con Firebase Authentication.
- Establecer su estado de disponibilidad (Disponible / No disponible).
- Ver su ubicación actual en un mapa.
- Consultar usuarios disponibles cercanos.
- Visualizar puntos de interés cargados desde un archivo JSON local.
- Recibir notificaciones relacionadas con la disponibilidad.

La aplicación integra servicios de Firebase con una interfaz básica en Android y usa OSMDroid para mostrar el mapa, junto con Google Play Services Location para obtener la ubicación del usuario.

## Características principales

- Autenticación con correo y contraseña
- Registro de usuarios
- Mapa de la ubicación actual del usuario
- Visualización de puntos de interés en el mapa
- Estado de disponibilidad en tiempo real
- Consulta de usuarios disponibles
- Notificaciones de servicio en segundo plano
- Soporte para permisos de ubicación y notificaciones

## Stack tecnológico

- Kotlin
- Android SDK
- Firebase Authentication
- Firebase Realtime Database
- Firebase Cloud Messaging / Notifications
- Firebase Storage
- Google Play Services Location
- OSMDroid
- Picasso
- Glide
- Material Components

## Estructura del proyecto

```text
Taller03/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/taller03/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   ├── AutenticacionActivity.kt
│   │   │   │   ├── RegistroActivity.kt
│   │   │   │   ├── MapaActivity.kt
│   │   │   │   ├── MapaUsuariosActivity.kt
│   │   │   │   ├── UsuariosDisponiblesActivity.kt
│   │   │   │   ├── UsuarioDisponibleService.kt
│   │   │   │   └── ...
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── drawable/
│   │   │   │   ├── values/
│   │   │   │   └── xml/
│   │   │   ├── AndroidManifest.xml
│   │   │   └── assets/
│   │   ├── androidTest/
│   │   └── test/
│   ├── build.gradle.kts
│   ├── google-services.json
│   └── proguard-rules.pro
├── build.gradle.kts
├── settings.gradle.kts
├── gradlew
├── gradlew.bat
├── gradle.properties
├── .gitignore
└── README.md
```

## Requisitos

- Android Studio (última versión estable recomendada)
- JDK 11+
- SDK Android 35
- Dispositivo físico o emulador con API 24+
- Cuenta de Firebase configurada

## Configuración

1. Clona el repositorio:

```bash
git clone https://github.com/Danielamn026/Taller03.git
cd Taller03
```

2. Abre el proyecto en Android Studio.

3. Sincroniza Gradle.

4. Agrega tu archivo `google-services.json` en la carpeta `app/` desde tu proyecto de Firebase.

5. En Firebase, habilita:
   - Authentication
   - Email/Password
   - Realtime Database
   - Firebase Cloud Messaging, si quieres usar notificaciones completas

6. Ejecuta la app desde Android Studio.

## Permisos requeridos

La aplicación solicita permisos de:

- Internet
- Ubicación precisa y aproximada
- Almacenamiento
- Notificaciones
- Foreground service

## Consideraciones

- El paquete base del proyecto es `com.example.taller03`.
- La app está pensada como prototipo/entregable académico con integración de ubicación y disponibilidad en tiempo real.
- El nombre del proyecto puede cambiarse al publicar una versión final más comercial o más formal.

## Cómo funciona la app

1. El usuario entra a la pantalla principal.
2. Puede registrarse o iniciar sesión.
3. Si ya está autenticado, se redirige a la pantalla del mapa.
4. Cuando se acepta el permiso de ubicación, la app obtiene la ubicación actual y la actualiza en Firebase.
5. El usuario puede cambiar su disponibilidad desde el menú.
6. La lista de usuarios disponibles puede consultarse desde el mapa.
7. El servicio en primer plano mantiene la disponibilidad activa en la aplicación.
- agregar pruebas unitarias o de UI
- mejorar validaciones y manejo de errores
- crear una versión final con branding propio
- documentar flujos de autenticación y de geolocalización

