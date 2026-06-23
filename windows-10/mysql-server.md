# Guía de instalación — MySQL Server 8.0 en Windows 10 utilizando WSL (Ubuntu 20.04.6 LTS)

## 1. Descripción

Esta guía explica el proceso de instalación y configuración inicial de MySQL Server 8.0 dentro de WSL (Windows Subsystem for Linux) utilizando Ubuntu 20.04.6 LTS.

Al finalizar esta guía será posible:

* Instalar MySQL Server.
* Iniciar el servicio de MySQL.
* Acceder al servidor desde la terminal.
* Configurar una contraseña para el usuario root.
* Verificar el funcionamiento del servidor.
* Conectarse posteriormente desde MySQL Workbench.

> IMPORTANTE:
>
> Se asume que WSL y Ubuntu 20.04.6 LTS ya se encuentran instalados y funcionando correctamente.

---

# 2. Arquitectura utilizada

## Entorno de trabajo

| Componente                  | Ubicación                |
| --------------------------- | ------------------------ |
| Sistema operativo principal | Windows 10               |
| Servidor MySQL              | Ubuntu 20.04.6 LTS (WSL) |
| Cliente gráfico             | MySQL Workbench          |

---

# 3. Abrir Ubuntu

## Paso 1

Abrir:

```text
Menú Inicio > Ubuntu 20.04.6 LTS
```

Se abrirá una terminal Linux.

---

# 4. Actualizar repositorios

Antes de instalar MySQL se recomienda actualizar la información de los paquetes disponibles.

Ejecutar:

```bash
sudo apt update
```

Cuando se solicite, ingresar la contraseña del usuario de Ubuntu.

---

# 5. Instalar MySQL Server

Ejecutar:

```bash
sudo apt install mysql-server -y
```

Esperar a que finalice la instalación.

---

# 6. Verificar instalación

Comprobar que MySQL fue instalado correctamente.

Ejecutar:

```bash
mysql --version
```

## Resultado esperado

Debe mostrarse información similar a:

```text
mysql  Ver 8.0.x for Linux on x86_64
```

---

# 7. Iniciar el servicio MySQL

Ejecutar:

```bash
sudo service mysql start
```

---

# 8. Verificar estado del servicio

Ejecutar:

```bash
sudo service mysql status
```

## Resultado esperado

Debe mostrarse información indicando que el servicio se encuentra:

```text
active (running)
```

---

# 9. Acceder a MySQL

En Ubuntu, después de la instalación, normalmente el usuario root utiliza autenticación mediante el sistema operativo.

Ingresar al servidor ejecutando:

```bash
sudo mysql
```

## Resultado esperado

Debe mostrarse el prompt de MySQL:

```sql
mysql>
```

---

# 10. Verificar usuarios existentes

Ejecutar:

```sql
SELECT User, Host
FROM mysql.user;
```

Se mostrará la lista de usuarios registrados.

---

# 11. Configurar contraseña para el usuario root

## IMPORTANTE

MySQL Workbench requiere autenticación mediante usuario y contraseña.

Por esta razón es necesario asignar una contraseña al usuario root.

Ejecutar:

```sql
ALTER USER 'root'@'localhost'
IDENTIFIED WITH mysql_native_password
BY 'Pa$$w0rd';
```

> Sustituir:
>
> ```text
> nueva_contrasena
> ```
>
> por la contraseña definida para el curso.

---

# 12. Aplicar cambios

Ejecutar:

```sql
FLUSH PRIVILEGES;
```

---

# 13. Salir de MySQL

Ejecutar:

```sql
EXIT;
```

---

# 14. Verificar acceso con la nueva contraseña

Intentar iniciar sesión nuevamente.

Ejecutar:

```bash
mysql -u root -p
```

## Paso siguiente

Ingresar la contraseña configurada anteriormente.

---

## Resultado esperado

Debe mostrarse:

```sql
mysql>
```

indicando que la autenticación fue exitosa.

---

# 15. Verificar funcionamiento del servidor

Ejecutar:

```sql
SELECT VERSION();
```

## Resultado esperado

Debe mostrarse una versión similar a:

```text
8.0.x
```

---

# 16. Verificar que MySQL acepte conexiones locales

Ejecutar:

```sql
SHOW DATABASES;
```

## Resultado esperado

Debe mostrarse una lista similar a:

```text
information_schema
mysql
performance_schema
sys
```

---

# 17. Configuración para MySQL Workbench

Una vez instalado MySQL Workbench, crear una nueva conexión utilizando:

## Connection Name

```text
Local MySQL
```

## Hostname

```text
localhost
```

## Port

```text
3306
```

## Username

```text
root
```

## Password

La contraseña configurada en el paso 11.

---

# 18. Probar conexión desde Workbench

Seleccionar:

```text
Test Connection
```

## Resultado esperado

Debe mostrarse un mensaje similar a:

```text
Successfully made the MySQL connection
```

---

# 19. Solución de problemas comunes

## El comando mysql no existe

Verificar que la instalación haya finalizado correctamente:

```bash
mysql --version
```

Si el comando no existe:

```bash
sudo apt install mysql-server -y
```

---

## El servicio no inicia

Intentar:

```bash
sudo service mysql restart
```

Posteriormente verificar:

```bash
sudo service mysql status
```

---

## Error de acceso para root

Verificar:

* Usuario correcto.
* Contraseña correcta.
* Que se haya ejecutado el comando ALTER USER correctamente.

---

## Workbench no puede conectarse

Verificar:

* Hostname = localhost
* Port = 3306
* Usuario = root
* Contraseña correcta

También confirmar que el servicio MySQL se encuentre en ejecución.

---

# 20. Referencias oficiales

## Microsoft WSL

https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-database

## MySQL

https://www.mysql.com/

## Documentación MySQL

https://dev.mysql.com/doc/

---

# 21. Conclusión

MySQL Server ha sido instalado y configurado correctamente dentro de Ubuntu 20.04.6 LTS ejecutándose sobre WSL en Windows 10.

Al finalizar esta guía se cuenta con:

* Un servidor MySQL funcional.
* Acceso mediante usuario root.
* Contraseña configurada para autenticación.
* Compatibilidad con MySQL Workbench.
* Entorno listo para desarrollar y administrar bases de datos durante el curso.
