# 🇨🇱 ESFOCAR App

Aplicación móvil Android de apoyo al estudio para la Escuela de Formación de Carabineros (ESFOCAR). El proyecto busca facilitar el repaso de contenidos y el acceso a material de estudio mediante una interfaz móvil con navegación, gestión local de usuarios y documentos.

> **Aviso:** este proyecto es un MVP académico y no está conectado a sistemas institucionales oficiales. No debe utilizarse para almacenar información sensible ni como sistema institucional.

## Funcionalidades

- Pantallas de bienvenida, registro e inicio de sesión.
- Navegación entre las secciones de la aplicación.
- Gestión de perfiles y usuarios con roles.
- Herramientas de administración para consultar, editar y eliminar cuentas de estudiantes y profesores.
- Gestión de documentos de estudio, incluyendo selección y apertura de archivos PDF.
- Persistencia local de datos con Room y SQLite.
- Interfaz construida con Jetpack Compose y Material Design 3.

La disponibilidad de algunas acciones puede depender del rol del usuario.

## Tecnologías

- **Kotlin** y **Android Studio**
- **Jetpack Compose** y **Material Design 3**
- **Navigation Compose** para la navegación
- **Room** con **SQLite** para almacenamiento local
- **KSP** para el procesamiento de código de Room
- **Gradle Kotlin DSL** para la configuración del proyecto

## Requisitos

- Android Studio compatible con Android Gradle Plugin 9.4.1.
- JDK 11 o una versión compatible con la configuración de Android Gradle Plugin instalada.
- Android SDK 37 para compilar el proyecto.
- Un emulador o dispositivo Android con API 26 o superior para ejecutar la aplicación.

## Configuración y ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/nat258/App-ESFOCAR.git
   cd App-ESFOCAR
   ```

2. Abre el proyecto en Android Studio y espera a que Gradle termine la sincronización.
3. Selecciona un emulador o conecta un dispositivo Android (API 26 o superior).
4. Ejecuta la configuración `app` desde Android Studio.

También puedes compilar desde la terminal con el Gradle Wrapper:

```bash
./gradlew assembleDebug
```

En Windows:

```bat
gradlew.bat assembleDebug
```

El APK de depuración se genera en `app/build/outputs/apk/debug/`.

## Estructura del proyecto

```text
.
├── app/
│   └── src/main/
│       ├── java/com/example/proyecto_esfocar/
│       │   ├── data/       # Acceso y persistencia de datos
│       │   ├── model/      # Modelos de la aplicación
│       │   ├── ui/         # Pantallas, componentes, navegación y tema
│       │   └── viewmodel/  # Estado y lógica de presentación
│       └── res/            # Recursos Android
├── gradle/                 # Catálogo de versiones y configuración de Gradle
├── build.gradle.kts
└── settings.gradle.kts
```

## Pruebas

Para ejecutar las pruebas locales disponibles:

```bash
./gradlew test
```

Para ejecutar las pruebas instrumentadas, con un emulador o dispositivo conectado:

```bash
./gradlew connectedAndroidTest
```

## Estado y alcance

Este repositorio es un proyecto académico en desarrollo. Las cuentas y los documentos se manejan localmente; la aplicación no autentica contra servicios institucionales ni sincroniza datos con un servidor.

## Licencia

No se ha especificado una licencia para este repositorio. Consulta al equipo propietario antes de reutilizar o distribuir el código.
