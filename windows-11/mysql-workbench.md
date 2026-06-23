# Guía de instalación — MySQL Workbench 8.0.47 en Windows 11

## 1. Descripción

Esta guía explica el proceso de descarga, instalación y configuración inicial de MySQL Workbench 8.0.47 en equipos con Windows 11.

MySQL Workbench es una herramienta gráfica utilizada para administrar bases de datos MySQL mediante una interfaz visual. Permite realizar tareas como:

* Administración de servidores MySQL.
* Ejecución de consultas SQL.
* Diseño y modelado de bases de datos.
* Gestión de usuarios y permisos.
* Importación y exportación de información.

---

# 2. Compatibilidad con Windows 11

La versión **MySQL Workbench 8.0.47** es compatible con:

* Windows 11 Home
* Windows 11 Pro
* Windows 11 Education
* Windows 11 Enterprise

## Arquitectura requerida

* 64 bits

> IMPORTANTE:
>
> MySQL Workbench no cuenta con versiones para sistemas operativos de 32 bits.

---

# 3. Requisitos recomendados

| Componente              | Recomendación                      |
| ----------------------- | ---------------------------------- |
| Sistema operativo       | Windows 11 64 bits                 |
| Procesador              | Intel Core i5 / Ryzen 5 o superior |
| Memoria RAM             | 8 GB mínimo                        |
| Memoria RAM recomendada | 16 GB                              |
| Espacio disponible      | 500 MB                             |
| Almacenamiento          | SSD recomendado                    |
| Resolución              | 1920 × 1080 recomendada            |

> Nota:
>
> Para administrar bases de datos locales es necesario contar con una instalación de MySQL Server.

---

# 4. Verificar arquitectura del sistema

## Paso 1

Abrir:

```text id="g6j8q1"
Configuración > Sistema > Acerca de
```

## Paso 2

Localizar:

```text id="z5v4kp"
Tipo de sistema
```

## Paso 3

Verificar que aparezca:

```text id="c3t7nr"
Sistema operativo de 64 bits
```

---

# 5. Descarga del instalador

## Sitio oficial

Descargar desde:

https://dev.mysql.com/downloads/workbench/

---

## Seleccionar

1. Microsoft Windows.
2. Windows (x86, 64-bit).
3. Versión 8.0.47.

El archivo descargado tendrá un nombre similar a:

```text id="u8n4mb"
mysql-workbench-community-8.0.47-winx64.msi
```

---

# 6. Instalación paso a paso

## Paso 1 — Ejecutar instalador

1. Localizar el archivo descargado.
2. Hacer clic derecho.
3. Seleccionar:

```text id="v7k3oa"
Ejecutar como administrador
```

---

## Paso 2 — Pantalla de bienvenida

Presionar:

```text id="y1f8eh"
Next
```

---

## Paso 3 — Seleccionar tipo de instalación

Elegir:

```text id="d9q2mx"
Complete
```

Esta opción instala todos los componentes recomendados.

Presionar:

```text id="r5c8tw"
Next
```

---

## Paso 4 — Confirmar instalación

Seleccionar:

```text id="j4n7zb"
Install
```

Esperar a que finalice la instalación.

---

## Paso 5 — Finalizar

Presionar:

```text id="m2w6kp"
Finish
```

---

## Resultado esperado

Debe mostrarse la versión instalada de MySQL Server.

Ejemplo:

```text id="a5t1re"
8.0.x
```

---

# Solución de problemas comunes

## No se puede establecer conexión

Verificar:

* Que MySQL Server esté instalado.
* Que el servicio MySQL esté iniciado.
* Que el puerto 3306 no esté bloqueado.

---

## Error de autenticación

Verificar:

* Usuario correcto.
* Contraseña correcta.
* Permisos del usuario configurados adecuadamente.

---

## Conexión rechazada

Confirmar que:

```text id="s9m3wv"
Hostname = localhost
Port = 3306
```

y que MySQL Server se encuentre en ejecución.

---

## La aplicación no inicia

Intentar:

* Ejecutar como administrador.
* Actualizar Windows 11.
* Reinstalar MySQL Workbench.

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

MySQL Workbench 8.0.47 proporciona una interfaz gráfica completa para administrar bases de datos MySQL de manera eficiente.

Para obtener la mejor experiencia de uso se recomienda:

* Windows 11 actualizado.
* 8 GB RAM como mínimo.
* SSD para mejorar el rendimiento.
* MySQL Server correctamente instalado y configurado.
