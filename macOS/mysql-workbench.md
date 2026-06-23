# Guía de instalación — MySQL Workbench 8.0.47 en macOS

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de MySQL Workbench 8.0.47 en equipos con macOS.

MySQL Workbench es una herramienta gráfica utilizada para administrar bases de datos MySQL mediante una interfaz visual. Permite realizar tareas como:

* Administración de servidores MySQL.
* Ejecución de consultas SQL.
* Diseño y modelado de bases de datos.
* Gestión de usuarios y permisos.
* Importación y exportación de información.

---

# 2. Compatibilidad con macOS

La versión **MySQL Workbench 8.0.47** es compatible con:

* macOS 13 Ventura o superior
* Equipos con procesadores Intel
* Equipos con Apple Silicon:

  * M1
  * M2
  * M3
  * M4
  * versiones posteriores

> IMPORTANTE:
>
> Se recomienda descargar la versión correspondiente a la arquitectura del equipo para obtener el mejor rendimiento.

---

# 3. Requisitos recomendados

| Componente              | Recomendación         |
| ----------------------- | --------------------- |
| Sistema operativo       | macOS 13 o superior   |
| Procesador              | Intel o Apple Silicon |
| Memoria RAM             | 8 GB mínimo           |
| Memoria RAM recomendada | 16 GB                 |
| Espacio disponible      | 500 MB                |
| Almacenamiento          | SSD recomendado       |
| Resolución              | 1440 × 900 o superior |

> Nota:
>
> Para conectarse a bases de datos locales será necesario contar con una instalación funcional de MySQL Server.

---

# 4. Verificar versión de macOS

## Paso 1

Abrir:

```text
Menú Apple > Acerca de esta Mac
```

## Paso 2

Verificar:

* Versión de macOS.
* Tipo de procesador o chip.

### Ejemplo para Apple Silicon

```text
Chip: Apple M2
```

### Ejemplo para Intel

```text
Processor: Intel Core i5
```

---

# 5. Descarga del instalador

## Sitio oficial

Descargar desde:

https://dev.mysql.com/downloads/workbench/

---

## Seleccionar la arquitectura correcta

### Equipos Apple Silicon

Seleccionar:

```text
macOS (ARM, 64-bit)
```

---

### Equipos Intel

Seleccionar:

```text
macOS (x86, 64-bit)
```

---

## Versión

Seleccionar:

```text
MySQL Workbench Community Edition 8.0.47
```

El archivo descargado tendrá un nombre similar a:

### Apple Silicon

```text
mysql-workbench-community-8.0.47-macos-arm64.dmg
```

### Intel

```text
mysql-workbench-community-8.0.47-macos-x86_64.dmg
```

---

# 6. Proceso de instalación

## Paso 1 — Abrir archivo DMG

1. Localizar el archivo descargado.
2. Hacer doble clic sobre el archivo `.dmg`.

---

## Paso 2 — Instalar aplicación

Aparecerá una ventana mostrando MySQL Workbench y la carpeta Applications.

Arrastrar:

```text
MySQLWorkbench.app
```

hacia:

```text
Applications
```

Esperar a que finalice la copia.

---

## Paso 3 — Abrir la aplicación

1. Abrir:

   ```text
   Launchpad
   ```

2. Buscar:

   ```text
   MySQL Workbench
   ```

3. Ejecutar la aplicación.

---

# 7. Permisos de seguridad de macOS

En algunos equipos macOS puede bloquear la primera ejecución.

## Solución

Abrir:

```text
Configuración del Sistema > Privacidad y seguridad
```

Seleccionar:

```text
Abrir de todos modos
```

y confirmar la ejecución de la aplicación.

---

# Solución de problemas comunes
## MySQL Workbench no abre

Verificar:

* Que la aplicación se encuentre en la carpeta Applications.
* Que se haya permitido la ejecución desde Privacidad y seguridad.
* Que macOS esté actualizado.

---

# Referencias oficiales

* MySQL Workbench:

https://dev.mysql.com/downloads/workbench/

* Documentación oficial:

https://dev.mysql.com/doc/workbench/en/

* MySQL Community Edition:

https://www.mysql.com/

---

# Conclusión

MySQL Workbench 8.0.47 proporciona una interfaz gráfica completa para la administración de bases de datos MySQL en macOS.

Para obtener la mejor experiencia de uso se recomienda:

* Utilizar una versión actualizada de macOS.
* Instalar la versión correspondiente a la arquitectura del equipo (Intel o Apple Silicon).
* Contar con al menos 8 GB de RAM.
* Utilizar almacenamiento SSD.
* Tener MySQL Server correctamente instalado y configurado.
