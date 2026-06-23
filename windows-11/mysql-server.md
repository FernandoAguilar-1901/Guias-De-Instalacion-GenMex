# Guía de instalación — MySQL Server 8.0 en Windows 11 utilizando WSL (Ubuntu 20.04.6 LTS)

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
| Sistema operativo principal | Windows 11               |
| Servidor MySQL              | Ubuntu 20.04.6 LTS (WSL) |
| Cliente gráfico             | MySQL Workbench          |

---

# 3. Abrir Ubuntu

## Paso 1

Abrir:

```text id="m5p4xe"
Menú Inicio > Ubuntu 20.04.6 LTS
```

Se abrirá una terminal Linux.

---

# 4. Actualizar repositorios

Antes de instalar MySQL se recomienda actualizar la información de los paquetes disponibles.

Ejecutar:

```bash id="g4j6wv"
sudo apt update
```

Cuando se solicite, ingresar la contraseña del usuario de Ubuntu.

---

# 5. Instalar MySQL Server

Ejecutar:

```bash id="n8z3fa"
sudo apt install mysql-server -y
```

Esperar a que finalice la instalación.

---

# 6. Verificar instalación

Comprobar que MySQL fue instalado correctamente.

Ejecutar:

```bash id="u7c9lr"
mysql --version
```

## Resultado esperado

Debe mostrarse información similar a:

```text id="s8x2ke"
mysql  Ver 8.0.x for Linux on x86_64
```

---

# 7. Iniciar el servicio MySQL

Ejecutar:

```bash id="f3n1yt"
sudo service mysql start
```

---

# 8. Verificar estado del servicio

Ejecutar:

```bash id="k9r6oq"
sudo service mysql status
```

## Resultado esperado

Debe mostrarse información indicando que el servicio se encuentra:

```text id="z5v7wd"
active (running)
```

---

# 9. Acceder a MySQL

En Ubuntu, después de la instalación, normalmente el usuario root utiliza autenticación mediante el sistema operativo.

Ingresar al servidor ejecutando:

```bash id="e1m8qh"
sudo mysql
```

## Resultado esperado

Debe mostrarse el prompt de MySQL:

```sql id="v2k4ba"
mysql>
```

---

# 10. Verificar usuarios existentes

Ejecutar:

```sql id="r7d3jp"
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

```sql id="q6u1nm"
ALTER USER 'root'@'localhost'
IDENTIFIED WITH mysql_native_password
BY 'Pa$$w0rd';
```

---

# 12. Aplicar cambios

Ejecutar:

```sql id="b5x9rt"
FLUSH PRIVILEGES;
```

---

# 13. Salir de MySQL

Ejecutar:

```sql id="c8j2fp"
EXIT;
```

---

# 14. Verificar acceso con la nueva contraseña

Intentar iniciar sesión nuevamente.

Ejecutar:

```bash id="d4y8ku"
mysql -u root -p
```

## Paso siguiente

Ingresar la contraseña configurada anteriormente.

---

## Resultado esperado

Debe mostrarse:

```sql id="a9h5ze"
mysql>
```

indicando que la autenticación fue exitosa.

---

# 15. Verificar funcionamiento del servidor

Ejecutar:

```sql id="w6n2sj"
SELECT VERSION();
```

## Resultado esperado

Debe mostrarse una versión similar a:

```text id="g1t8mv"
8.0.x
```

---

# 16. Verificar que MySQL acepte conexiones locales

Ejecutar:

```sql id="p4c7yr"
SHOW DATABASES;
```

## Resultado esperado

Debe mostrarse una lista similar a:

```text id="j8e4on"
information_schema
mysql
performance_schema
sys
```

---

# 17. Configuración para MySQL Workbench

Una vez instalado MySQL Workbench, crear una nueva conexión utilizando:

## Connection Name

```text id="n6w3hb"
Local MySQL
```

## Hostname

```text id="x2k9fa"
localhost
```

## Port

```text id="m7d5qv"
3306
```

## Username

```text id="r4p8yu"
root
```

## Password

La contraseña configurada en el paso 11.

---

# 18. Probar conexión desde Workbench

Seleccionar:

```text id="h3t6cz"
Test Connection
```

## Resultado esperado

Debe mostrarse un mensaje similar a:

```text id="k7v1bx"
Successfully made the MySQL connection
```

---

# 19. Solución de problemas comunes

## El comando mysql no existe

Verificar que la instalación haya finalizado correctamente:

```bash id="o9f2jm"
mysql --version
```

Si el comando no existe:

```bash id="u5n7wd"
sudo apt install mysql-server -y
```

---

## El servicio no inicia

Intentar:

```bash id="y8r4kl"
sudo service mysql restart
```

Posteriormente verificar:

```bash id="v1c9ts"
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

MySQL Server ha sido instalado y configurado correctamente dentro de Ubuntu 20.04.6 LTS ejecutándose sobre WSL en Windows 11.

Al finalizar esta guía se cuenta con:

* Un servidor MySQL funcional.
* Acceso mediante usuario root.
* Contraseña configurada para autenticación.
* Compatibilidad con MySQL Workbench.
* Entorno listo para desarrollar y administrar bases de datos durante el curso.
