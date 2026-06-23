# Guía de instalación — MySQL Workbench 8.0.47 en Windows 10

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de MySQL Workbench 8.0.47 en equipos con Windows 10.

MySQL Workbench es una herramienta gráfica que permite administrar bases de datos MySQL mediante una interfaz visual. Entre sus principales funciones se encuentran:

* Administración de servidores MySQL.
* Diseño de modelos de bases de datos.
* Ejecución de consultas SQL.
* Gestión de usuarios y permisos.
* Importación y exportación de datos.

---

# 2. Compatibilidad con Windows 10

La versión **MySQL Workbench 8.0.47** es compatible con:

* Windows 10 de 64 bits
* Windows 10 versión 1809 o superior

> IMPORTANTE:
>
> MySQL Workbench no ofrece soporte para sistemas operativos de 32 bits.

## Recomendación

Se recomienda utilizar:

* Windows 10 versión 21H2 o superior
* 8 GB de RAM o más
* Unidad SSD para mejorar el rendimiento

---

# 3. Verificar versión de Windows

## Paso 1

Presionar:

```text
Windows + R
```

## Paso 2

Escribir:

```text
winver
```

## Paso 3

Verificar que:

* El sistema operativo sea Windows 10.
* La versión sea 1809 o superior.

---

# 4. Requisitos mínimos

| Componente              | Requisito          |
| ----------------------- | ------------------ |
| Sistema operativo       | Windows 10 64 bits |
| Procesador              | x64                |
| Memoria RAM             | 4 GB mínimo        |
| Memoria RAM recomendada | 8 GB o más         |
| Espacio disponible      | 500 MB             |
| Resolución              | 1280 × 720 mínimo  |

> Nota:
>
> Para conectarse a bases de datos locales será necesario tener instalado MySQL Server.

---

# 5. Descarga del instalador

## Sitio oficial

Descargar desde:

https://dev.mysql.com/downloads/workbench/

## Seleccionar

1. Microsoft Windows.
2. Windows (x86, 64-bit).
3. Versión 8.0.47.

El archivo descargado tendrá un nombre similar a:

```text
mysql-workbench-community-8.0.47-winx64.msi
```

---

# 6. Proceso de instalación

## Paso 1 — Ejecutar instalador

1. Localizar el archivo descargado.
2. Hacer clic derecho.
3. Seleccionar:

```text
Ejecutar como administrador
```

---

## Paso 2 — Pantalla de bienvenida

Presionar:

```text
Next
```

---

## Paso 3 — Tipo de instalación

Seleccionar:

```text
Complete
```

Esta opción instala todos los componentes recomendados.

Presionar:

```text
Next
```

---

## Paso 4 — Confirmar instalación

Presionar:

```text
Install
```

Esperar a que finalice el proceso.

---

## Paso 5 — Finalizar

Presionar:

```text
Finish
```

---

# Solución de problemas comunes

## No puede conectarse al servidor

Verificar:

* Que MySQL Server esté instalado.
* Que el servicio esté iniciado.
* Que el puerto 3306 esté disponible.

---

## Error de contraseña

Verificar:

* Usuario correcto.
* Contraseña correcta.
* Permisos del usuario.

---

## La conexión es rechazada

Comprobar:

```text
Hostname = localhost
Port = 3306
```

y que el servicio MySQL se encuentre en ejecución.

---

## MySQL Workbench no inicia

Verificar:

* Actualizaciones de Windows.
* Permisos de administrador.
* Reinstalar la aplicación si es necesario.

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

MySQL Workbench 8.0.47 es una herramienta gráfica que simplifica la administración de bases de datos MySQL mediante una interfaz intuitiva.

Para obtener el mejor rendimiento se recomienda:

* Windows 10 actualizado.
* 8 GB RAM o más.
* Unidad SSD.
* MySQL Server instalado y configurado correctamente.
