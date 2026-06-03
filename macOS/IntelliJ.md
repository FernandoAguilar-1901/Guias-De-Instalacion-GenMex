# Guía de instalación — IntelliJ IDEA Community Edition 2025.2.6.1 en macOS

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de IntelliJ IDEA Community Edition 2025.2.6.1 en equipos con macOS.

IntelliJ IDEA es un entorno de desarrollo integrado (IDE) enfocado principalmente en desarrollo con Java y Kotlin, con soporte adicional para múltiples tecnologías mediante plugins.

---

# 2. Compatibilidad con macOS

La versión **IntelliJ IDEA 2025.2.6.1 Community Edition** es compatible con:

* macOS 13 Ventura o superior
* Procesadores Intel
* Apple Silicon:

  * M1
  * M2
  * M3
  * versiones posteriores

> IMPORTANTE:
>
> Se recomienda utilizar la versión nativa para Apple Silicon en equipos con procesadores M-series para obtener mejor rendimiento y menor consumo energético.

---

# 3. Requisitos recomendados

| Componente        | Recomendación                    |
| ----------------- | -------------------------------- |
| Sistema operativo | macOS 13 o superior              |
| Procesador        | Intel o Apple Silicon            |
| Memoria RAM       | 8 GB mínimo (16 GB recomendados) |
| Espacio en disco  | 10 GB libres                     |
| Almacenamiento    | SSD recomendado                  |
| Resolución        | 1440 × 900 o superior            |

---

# 4. Verificar versión de macOS

## Paso 1

Abrir:

```text id="m6q4sa"
Menú Apple > Acerca de esta Mac
```

## Paso 2

Verificar:

* Versión del sistema operativo
* Tipo de procesador

Ejemplos:

```text id="o5m3ru"
Apple M2
```

o

```text id="f1h9zv"
Intel Core i5
```

---

# 5. Descarga del instalador

## Sitio oficial

Descargar IntelliJ IDEA desde:

https://www.jetbrains.com/es-es/idea/download/?section=mac

1. Otras versiones (parte derecha de la pantalla)
2. Buscar versión 2025.2 > 2025.2.6.1
3. Seleccionar "MacOS" y "Community Edition"
4. Las instrucciones continúan en la siguiente sección
---

## Seleccionar versión correcta

### Equipos Apple Silicon

Seleccionar:

```text id="n2j8cy"
macOS (Apple Silicon)
```

---

### Equipos Intel

Seleccionar:

```text id="y4k1ta"
macOS (Intel)
```

---

## Community Edition

Seleccionar:

```text id="w3e7pi"
Community Edition
```

El archivo descargado normalmente será:

```text id="c8q2vs"
ideaIC-2025.2.6.1.dmg
```

---

# 6. Proceso de instalación

## Paso 1 — Abrir archivo DMG

1. Localizar el archivo descargado.
2. Hacer doble clic sobre:

   ```text
   ideaIC-2025.2.6.1.dmg
   ```

---

## Paso 2 — Arrastrar a Applications

1. Aparecerá una ventana con IntelliJ IDEA.
2. Arrastrar el icono hacia:

   ```text
   Applications
   ```

Esperar a que finalice la copia.

---

## Paso 3 — Abrir IntelliJ IDEA

1. Abrir:

   ```text
   Launchpad
   ```

2. Buscar:

   ```text
   IntelliJ IDEA Community Edition
   ```

3. Ejecutar la aplicación.

---

# 7. Permiso de seguridad de macOS

En algunos casos macOS mostrará una advertencia de seguridad.

## Solución

1. Abrir:

   ```text
   Configuración del Sistema > Privacidad y seguridad
   ```

2. Seleccionar:

   ```text
   Abrir de todos modos
   ```

3. Confirmar la ejecución.

---

# 8. Configuración inicial

## Importar configuraciones

Si es la primera instalación:

Seleccionar:

```text id="d7u5qo"
Do not import settings
```

---

## Política de privacidad

Aceptar:

* Política de privacidad
* Términos correspondientes

---

## Selección de tema

Elegir:

* Darcula (oscuro)
* Light (claro)

---

# 9. Instalación del JDK

## IMPORTANTE

Para desarrollar aplicaciones Java es necesario instalar un JDK.

---

## Recomendación

Instalar:

* Eclipse Temurin JDK 21
* OpenJDK 21

---

## Descarga sugerida

https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html

---

# 10. Verificar arquitectura del JDK

## Apple Silicon

Se recomienda descargar:

```text id="b6v9rc"
macOS AArch64
```

---

## Intel

Se recomienda descargar:

```text id="e1n2lw"
macOS x64
```

---

# 11. Configuración del JDK en IntelliJ

## Paso 1

Abrir IntelliJ IDEA.

---

## Paso 2

Seleccionar:

```text id="u9j4xf"
New Project
```

---

## Paso 3

En:

```text id="r5c1op"
Project SDK
```

Seleccionar el JDK instalado.

---

## Paso 4 — Agregar manualmente

Si no aparece:

1. Presionar:

   ```text
   Add JDK
   ```

2. Seleccionar la ruta correspondiente.

Ejemplo:

```text id="v2h7ad"
/Library/Java/JavaVirtualMachines/temurin-21.jdk
```

---

# 12. Verificar funcionamiento

## Crear proyecto de prueba

1. Crear un nuevo proyecto Java.

2. Crear archivo:

   ```java
   Main.java
   ```

3. Agregar:

```java id="t4n8jk"
public class Main {

    public static void main(String[] args) {
        System.out.println("Hola IntelliJ");
    }

}
```

4. Ejecutar el proyecto.

---

## Resultado esperado

```text id="k7z3cm"
Hola IntelliJ
```

---

# 13. Solución de problemas comunes

## macOS bloquea la aplicación

Abrir:

```text id="x3d5be"
Configuración del Sistema > Privacidad y seguridad
```

y permitir la ejecución.

---

## IntelliJ funciona lento

Recomendaciones:

* Utilizar SSD
* Tener 16 GB RAM para proyectos grandes
* Ajustar memoria desde:

  ```text
  Help > Change Memory Settings
  ```

---

## El JDK no aparece

Verificar:

* Que el JDK corresponda a la arquitectura correcta
* Que esté instalado correctamente
* Reiniciar IntelliJ

---

# 14. Referencias oficiales

* JetBrains:
  https://www.jetbrains.com/idea/

* Guía oficial:
  https://www.jetbrains.com/help/idea/installation-guide.html

* Eclipse Temurin:
  https://adoptium.net/

---

# 15. Conclusión

IntelliJ IDEA Community Edition 2025.2.6.1 es totalmente compatible con macOS moderno tanto en equipos Intel como Apple Silicon.

Para obtener la mejor experiencia de desarrollo se recomienda:

* macOS actualizado
* SSD
* 16 GB RAM
* JDK 21 nativo para la arquitectura del equipo
