# IYR Common Library — Maven público

Repositorio de paquetes Kotlin Multiplatform para Android e iOS. La descarga no requiere usuario ni token.

URL Maven: https://romancanoniero.github.io/iyrcommonlib-maven

En `settings.gradle.kts`, agregar dentro de `dependencyResolutionManagement.repositories`:

```kotlin
maven {
    url = uri("https://romancanoniero.github.io/iyrcommonlib-maven")
    content { includeGroup("io.github.romancanoniero") }
}
```

En las dependencias `commonMain` del módulo compartido:

```kotlin
implementation("io.github.romancanoniero:iyrcommonlib:0.1.2")
```

Gradle selecciona el AAR Android o el KLIB iOS correspondiente. Se incluyen Android API 23+, iOS ARM64, simulador ARM64 y simulador x64; iOS 14+. Compilado con Kotlin 2.3.0, AGP 8.13.2, Gradle 8.13 y JDK 17.

```kotlin
import com.iyr.iyrcommonlib.kmp.Platform
import com.iyr.iyrcommonlib.kmp.PlatformType

val android = Platform.isAndroid
val ios = Platform.isIOS
val current: PlatformType = Platform.current
```

Los paquetes incluyen modelos y utilidades KMP, fuentes KMP para navegación del IDE, documentación, licencia MIT, firmas PGP y sumas de verificación. Las vistas e integraciones del código Android histórico no forman parte de esta distribución. El repositorio fuente original permanece privado.

Las versiones publicadas se conservan sin sobrescribir. Cada archivo de `releases/<version>.sha256` enumera las rutas y hashes de esa versión; una versión está disponible cuando su manifiesto y sus paquetes aparecen publicados. La clave pública de firma está en `keys/iyrcommonlib.asc`.

Huella PGP: `C4DF0DFB9CE29BA83CF32B3BA3AEC4CF4B8C2853`.

Este es un repositorio Maven independiente alojado en GitHub Pages; no es Maven Central.
