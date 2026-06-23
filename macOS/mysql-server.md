# Guía de instalación — MySQL Server 8.0 en macOS utilizando Homebrew

## 1. Descripción

Esta guía explica el proceso de instalación y configuración inicial de MySQL Server 8.0 en macOS utilizando Homebrew.

Al finalizar esta guía será posible:

* Instalar MySQL Server.
* Iniciar el servicio de MySQL.
* Acceder al servidor desde la terminal.
* Configurar una contraseña para el usuario root.
* Verificar el funcionamiento del servidor.
* Conectarse posteriormente desde MySQL Workbench.

> IMPORTANTE:
>
> Se asume que Homebrew ya se encuentra instalado y funcionando correctamente.

---

# 2. Arquitectura utilizada

## Entorno de trabajo

| Componente         | Ubicación        |
| ------------------ | ---------------- |
| Sistema operativo  | macOS            |
| Gestor de paquetes | Homebrew         |
| Servidor MySQL     | MySQL Server 8.0 |
| Cliente gráfico    | MySQL Workbench  |

---

# 3. Verificar Homebrew

## Paso 1

Abrir la aplicación:

```text id="g7w2xa"
Terminal
```

## Paso 2

Verificar que Homebrew se encuentre instalado.

Ejecutar:

```bash id="j6m4ns"
brew --version
```

## Resultado esperado

Debe mostrarse información similar a:

```text id="z4c8ye"
Homebrew 4.x.x
```

---

# 4. Actualizar Homebrew

Antes de instalar MySQL se recomienda actualizar Homebrew.

Ejecutar:

```bash id="v8n1pk"
brew update
```

Esperar a que finalice la actualización.

---

# 5. Instalar MySQL Server

Ejecutar:

```bash id="d2r9mj"
brew install mysql
```

La descarga e instalación pueden tardar varios minutos dependiendo de la velocidad de Internet.

---

# 6. Verificar instalación

Comprobar que MySQL fue instalado correctamente.

Ejecutar:

```bash id="x5q7tv"
mysql --version
```

## Resultado esperado

Debe mostrarse información similar a:

```text id="m3f1ba"
mysql  Ver 8.0.x
```

---

# 7. Iniciar el servicio MySQL

Ejecutar:

```bash id="c9k6pu"
brew services start mysql
```

---

# 8. Verificar estado del servicio

Ejecutar:

```bash id="y4j8nh"
brew services list
```

## Resultado esperado

Debe mostrarse una línea similar a:

```text id="e7t5dr"
mysql started
```

---

# 9. Acceder a MySQL

Abrir una sesión en MySQL ejecutando:

```bash id="r6u2fw"
mysql -u root
```

## Resultado esperado

Debe mostrarse el prompt:

```sql id="w9m3cb"
mysql>
```

---

# 10. Verificar usuarios existentes

Ejecutar:

```sql id="h2v7qn"
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

```sql id="p8n4yr"
ALTER USER 'root'@'localhost'
IDENTIFIED BY 'nueva_contrasena';
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

```sql id="f5c1zx"
FLUSH PRIVILEGES;
```

---

# 13. Salir de MySQL

Ejecutar:

```sql id="a3k8wd"
EXIT;
```

---

# 14. Verificar acceso con la nueva contraseña

Intentar iniciar sesión nuevamente.

Ejecutar:

```bash id="q7m2rt"
mysql -u root -p
```

## Paso siguiente

Ingresar la contraseña configurada anteriormente.

---

## Resultado esperado

Debe mostrarse:

```sql id="u1v9ke"
mysql>
```

indicando que la autenticación fue exitosa.

---

# 15. Verificar funcionamiento del servidor

Ejecutar:

```sql id="b6t4mx"
SELECT VERSION();
```

## Resultado esperado

Debe mostrarse una versión similar a:

```text id="d9p7aj"
8.0.x
```

---

# 16. Verificar bases de datos disponibles

Ejecutar:

```sql id="s8e3qn"
SHOW DATABASES;
```

## Resultado esperado

Debe mostrarse una lista similar a:

```text id="n4r2cz"
information_schema
mysql
performance_schema
sys
```

---

# 17. Configuración para MySQL Workbench

Una vez instalado MySQL Workbench, crear una nueva conexión utilizando:

## Connection Name

```text id="g2j5mf"
Local MySQL
```

## Hostname

```text id="r8k4tu"
localhost
```

## Port

```text id="z3n7wp"
3306
```

## Username

```text id="m5v2ha"
root
```

## Password

La contraseña configurada en el paso 11.

---

# 18. Probar conexión desde Workbench

Seleccionar:

```text id="j1c6py"
Test Connection
```

## Resultado esperado

Debe mostrarse un mensaje similar a:

```text id="h7q3rn"
Successfully made the MySQL connection
```

---

# 19. Administración básica del servicio

## Detener MySQL

Ejecutar:

```bash id="t2m9vw"
brew services stop mysql
```

---

## Reiniciar MySQL

Ejecutar:

```bash id="c4r8yk"
brew services restart mysql
```

---

## Verificar servicios

Ejecutar:

```bash id="v6p1sb"
brew services list
```

---

# 20. Solución de problemas comunes

## El comando mysql no existe

Verificar la instalación:

```bash id="e9j7mn"
mysql --version
```

Si el comando no existe:

```bash id="y3v6pt"
brew install mysql
```

---

## El servicio no inicia

Intentar:

```bash id="u5k2fr"
brew services restart mysql
```

Posteriormente verificar:

```bash id="q9n4cx"
brew services list
```

---

## Error de acceso para root

Verificar:

* Usuario correcto.
* Contraseña correcta.
* Que el comando ALTER USER se haya ejecutado correctamente.

---

## Workbench no puede conectarse

Verificar:

* Hostname = localhost
* Port = 3306
* Usuario = root
* Contraseña correcta

También confirmar que el servicio MySQL se encuentre iniciado.

---

# 21. Referencias oficiales

## Homebrew Formula

https://formulae.brew.sh/formula/mysql

## MySQL

https://www.mysql.com/

## Documentación MySQL

https://dev.mysql.com/doc/

---

# 22. Conclusión

MySQL Server ha sido instalado y configurado correctamente en macOS utilizando Homebrew.

Al finalizar esta guía se cuenta con:

* Un servidor MySQL funcional.
* Acceso mediante usuario root.
* Contraseña configurada para autenticación.
* Compatibilidad con MySQL Workbench.
* Entorno listo para desarrollar y administrar bases de datos durante el curso.
