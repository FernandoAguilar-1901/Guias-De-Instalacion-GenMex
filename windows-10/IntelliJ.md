# Guía de instalación — IntelliJ IDEA Community Edition 2025.2.6.1 en Windows 10

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de IntelliJ IDEA Community Edition 2025.2.6.1 en equipos con Windows 10.

IntelliJ IDEA es un entorno de desarrollo integrado (IDE) enfocado principalmente en desarrollo con Java y Kotlin, aunque también soporta otros lenguajes y herramientas mediante plugins.

---

# 2. Compatibilidad con Windows 10

La versión **IntelliJ IDEA 2025.2.6.1 Community Edition** es compatible con:

* Windows 10 de 64 bits
* Windows 10 versión 1809 o superior

> IMPORTANTE:
>
> No existe soporte oficial para versiones de 32 bits.

## Recomendación

Se recomienda utilizar:

* Windows 10 versión 21H2 o superior
* 8 GB de RAM mínimo
* Unidad SSD para mejor rendimiento

## Verificar versión de Windows

1. Presionar:

   ```text
   Windows + R
   ```

2. Escribir:

   ```text
   winver
   ```

3. Confirmar que:

   * El sistema sea Windows 10
   * La versión sea 1809 o superior

---

# 3. Requisitos mínimos

| Componente        | Requisito mínimo                                     |
| ----------------- | ---------------------------------------------------- |
| Sistema operativo | Windows 10 64 bits                                   |
| Procesador        | x64 de 4 núcleos                                     |
| Memoria RAM       | 8 GB recomendados                                    |
| Espacio en disco  | 10 GB disponibles                                    |
| Resolución        | 1280 × 720 mínimo                                    |
| Java              | No es necesario instalar Java para ejecutar IntelliJ |

> IntelliJ incluye internamente JetBrains Runtime (JBR).

---

# 4. Descarga del instalador

## Sitio oficial

Descargar desde:

https://www.jetbrains.com/es-es/idea/download/?section=windows

## Seleccionar

1. Otras versiones (parte derecha de la pantalla)
2. Buscar versión 2025.2 > 2025.2.6.1
3. Seleccionar "Windows" y "Community Edition"
4. Descargar el archivo `.exe`

El instalador normalmente tendrá un nombre similar a:

```text
ideaIC-2025.2.6.1.exe
```

---

# 5. Proceso de instalación

## Paso 1 — Ejecutar instalador

1. Localizar el archivo descargado.
2. Ejecutar como administrador.

---

## Paso 2 — Pantalla de bienvenida

1. Presionar:

   ```text
   Next
   ```

---

## Paso 3 — Seleccionar ubicación

Se recomienda mantener la ruta por defecto:

```text
C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2025.2.6.1
```

Presionar:

```text
Next
```

---

## Paso 4 — Configuración adicional

Se recomienda activar:

* Create Desktop Shortcut
* Update PATH Variable
* Add "Open Folder as Project"
* Asociar archivos `.java`

Opcionalmente:

* Asociar archivos `.kt` para Kotlin

Presionar:

```text
Next
```

---

## Paso 5 — Carpeta del menú inicio

Mantener el nombre por defecto:

```text
JetBrains
```

Presionar:

```text
Install
```

---

## Paso 6 — Finalizar instalación

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

# 6. Configuración inicial

## Importar configuración

Si es la primera instalación:

```text
Do not import settings
```

---

## Política de privacidad

Aceptar los términos correspondientes.

---

## Configuración visual

Seleccionar:

* Tema oscuro (Darcula)
* Tema claro (Light)

Según preferencia del usuario.

---

# 7. Instalación del JDK

## IMPORTANTE

Aunque IntelliJ puede ejecutarse sin instalar Java manualmente, para desarrollar aplicaciones Java sí se requiere un JDK.

## Recomendación

Instalar:

* OpenJDK 21
* Temurin JDK 21

## Descarga sugerida

https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html

---

# 8. Configurar JDK en IntelliJ

1. Abrir IntelliJ IDEA.

2. Seleccionar:

   ```text
   New Project
   ```

3. En:

   ```text
   Project SDK
   ```

   seleccionar el JDK instalado.

Si no aparece:

1. Presionar:

   ```text
   Add JDK
   ```
2. Seleccionar la carpeta del JDK.

Ejemplo:

```text
C:\Program Files\Eclipse Adoptium\jdk-21
```

---

# 9. Verificar funcionamiento

## Crear proyecto de prueba

1. Crear un nuevo proyecto Java.

2. Crear archivo:

   ```java
   Main.java
   ```

3. Agregar:

```java
public class Main {

    public static void main(String[] args) {
        System.out.println("Hola IntelliJ");
    }

}
```

4. Ejecutar el programa.

## Resultado esperado

```text
Hola IntelliJ
```

---

# 10. Solución de problemas comunes

## El instalador no abre

Verificar:

* Que Windows sea de 64 bits
* Tener permisos de administrador
* Desactivar temporalmente antivirus si bloquea la ejecución

---

## IntelliJ funciona lento

Recomendaciones:

* Usar SSD
* Tener al menos 8 GB RAM
* Cerrar aplicaciones pesadas
* Aumentar memoria del IDE desde:

  ```text
  Help > Change Memory Settings
  ```

---

## No detecta el JDK

Verificar:

* Que el JDK esté correctamente instalado
* Que se seleccione la carpeta raíz del JDK
* Reiniciar IntelliJ

---

# 11. Referencias oficiales

* JetBrains:
  https://www.jetbrains.com/idea/

* Documentación:
  https://www.jetbrains.com/help/idea/installation-guide.html

* Eclipse Temurin:
  https://adoptium.net/

---

# 12. Conclusión

IntelliJ IDEA Community Edition 2025.2.6.1 es compatible con Windows 10 de 64 bits y ofrece un entorno robusto para desarrollo Java y Kotlin.

Para obtener el mejor rendimiento se recomienda utilizar:

* Windows 10 actualizado
* 8 GB RAM o más
* SSD
* JDK 21
