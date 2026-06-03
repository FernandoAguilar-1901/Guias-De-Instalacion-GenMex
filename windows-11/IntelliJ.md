# Guía de instalación — IntelliJ IDEA Community Edition 2025.2.6.1 en Windows 11

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de IntelliJ IDEA Community Edition 2025.2.6.1 en equipos con Windows 11.

IntelliJ IDEA es un entorno de desarrollo integrado (IDE) enfocado principalmente en desarrollo con Java y Kotlin, ofreciendo además soporte para múltiples tecnologías mediante plugins.

---

# 2. Compatibilidad con Windows 11

La versión **IntelliJ IDEA 2025.2.6.1 Community Edition** es totalmente compatible con:

* Windows 11 Home
* Windows 11 Pro
* Windows 11 Education
* Windows 11 Enterprise

## Arquitectura requerida

* 64 bits únicamente

> IMPORTANTE:
>
> IntelliJ IDEA no ofrece soporte para sistemas operativos de 32 bits.

---

# 3. Requisitos recomendados

| Componente        | Recomendación                      |
| ----------------- | ---------------------------------- |
| Sistema operativo | Windows 11 64 bits                 |
| Procesador        | Intel Core i5 / Ryzen 5 o superior |
| Memoria RAM       | 8 GB mínimo (16 GB recomendados)   |
| Espacio en disco  | 10 GB libres                       |
| Almacenamiento    | SSD recomendado                    |
| Resolución        | 1920 × 1080 recomendada            |

---

# 4. Verificar arquitectura del sistema

## Paso 1

Abrir:

```text id="m9j7o2"
Configuración > Sistema > Acerca de
```

## Paso 2

Verificar:

```text id="kw1wja"
Tipo de sistema
```

Debe indicar:

```text id="qv52mk"
Sistema operativo de 64 bits
```

---

# 5. Descarga del instalador

## Sitio oficial

Descargar IntelliJ IDEA desde:

https://www.jetbrains.com/es-es/idea/download/?section=windows

## Seleccionar

1. Otras versiones (parte derecha de la pantalla)
2. Buscar versión 2025.2 > 2025.2.6.1
3. Seleccionar "Windows" y "Community Edition"
4. Descargar el archivo `.exe`

Nombre aproximado del archivo:

```text id="a2vqke"
ideaIC-2025.2.6.1.exe
```

---

# 6. Instalación paso a paso

## Paso 1 — Ejecutar instalador

1. Localizar el archivo descargado.
2. Hacer clic derecho.
3. Seleccionar:

   ```text
   Ejecutar como administrador
   ```

---

## Paso 2 — Pantalla inicial

Presionar:

```text id="c5dbng"
Next
```

---

## Paso 3 — Ruta de instalación

Se recomienda conservar la ruta predeterminada:

```text id="v6b5b4"
C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2025.2.6.1
```

Presionar:

```text id="k9xv13"
Next
```

---

## Paso 4 — Opciones adicionales

Se recomienda habilitar:

* Create Desktop Shortcut
* Update PATH Variable
* Add "Open Folder as Project"
* Asociar archivos `.java`

Opcionalmente:

* Asociar archivos `.kt` para Kotlin

Presionar:

```text id="pwf2ec"
Next
```

---

## Paso 5 — Menú inicio

Mantener:

```text id="4z1b9u"
JetBrains
```

Presionar:

```text id="8m4qfy"
Install
```

---

## Paso 6 — Finalizar

1. Esperar a que termine la instalación.
2. Activar:

   ```text
   Run IntelliJ IDEA Community Edition
   ```
3. Presionar:

   ```text
   Finish
   ```

---

# 7. Configuración inicial

## Importar configuraciones

Si es la primera vez instalando IntelliJ:

Seleccionar:

```text id="p1nh8u"
Do not import settings
```

---

## Aceptar políticas

Aceptar:

* Política de privacidad
* Acuerdos de licencia correspondientes

---

## Selección de tema

Elegir entre:

* Darcula (oscuro)
* Light (claro)

---

# 8. Instalación del JDK

## IMPORTANTE

Para desarrollar aplicaciones Java se requiere instalar un JDK adicional.

## Recomendación

Instalar:

* Eclipse Temurin JDK 21
* OpenJDK 21

## Descarga sugerida

https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html

---

# 9. Configuración del JDK en IntelliJ

## Paso 1

Abrir IntelliJ IDEA.

---

## Paso 2

Seleccionar:

```text
New Project
```

---

## Paso 3

En:

```text
Project SDK
```

Seleccionar el JDK instalado.

---

## Paso 4 — Agregar manualmente (si no aparece)

1. Presionar:

   ```text
   Add JDK
   ```

2. Seleccionar la carpeta del JDK.

Ejemplo:

```text id="q4i8ho"
C:\Program Files\Eclipse Adoptium\jdk-21
```

---

# 10. Verificar instalación

## Crear proyecto de prueba

1. Crear un proyecto Java.

2. Crear archivo:

   ```java
   Main.java
   ```

3. Agregar:

```java id="tkt7ha"
public class Main {

    public static void main(String[] args) {
        System.out.println("Hola IntelliJ");
    }

}
```

4. Ejecutar el proyecto.

---

## Resultado esperado

```text id="s4iylt"
Hola IntelliJ
```

---

# 11. Solución de problemas comunes

## El instalador no inicia

Verificar:

* Tener permisos de administrador
* Que Windows esté actualizado
* Que el antivirus no bloquee la instalación

---

## IntelliJ funciona lento

Recomendaciones:

* Utilizar SSD
* Incrementar memoria RAM asignada
* Cerrar aplicaciones pesadas
* Ajustar memoria desde:

  ```text
  Help > Change Memory Settings
  ```

---

## No aparece el JDK

Verificar:

* Que el JDK esté correctamente instalado
* Seleccionar la carpeta raíz correcta
* Reiniciar IntelliJ

---

# 12. Referencias oficiales

* JetBrains:
  https://www.jetbrains.com/idea/

* Guía oficial:
  https://www.jetbrains.com/help/idea/installation-guide.html

* Eclipse Temurin:
  https://adoptium.net/

---

# 13. Conclusión

IntelliJ IDEA Community Edition 2025.2.6.1 es completamente compatible con Windows 11 y proporciona un entorno moderno y robusto para desarrollo Java y Kotlin.

Para obtener la mejor experiencia de desarrollo se recomienda:

* Windows 11 actualizado
* SSD
* 16 GB RAM
* JDK 21
