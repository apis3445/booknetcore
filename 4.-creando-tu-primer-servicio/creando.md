# 4.1 Crear las base de datos y los usuarios en MySQL

Primero vamos a crear la base de datos y los usuarios para conectarnos la base de datos.

{% hint style="warning" %}
Por seguridad NO se recomienda que el usuario root  \(MySQL\) o sa \(SQL Server\) se conecte a la base de datos desde tu aplicación.
{% endhint %}

 En mi caso creare un usuario administrador para crear las tablas en la base de datos y un usuario de solo lectura con acceso a solo realizar selects, inserts, updates y deletes, desde los servicios REST nos conectaremos con el usuario de lectura.

### 4.1.1 Creando la base de datos y los usuarios en MySQL

Primero vamos a crear la base de datos

1. Con el editor de MySQL tecleamos el siguiente comando para crear la base de datos `CREATE DATABASE caduca CHARACTER SET utf8 COLLATE utf8_general_ci;`
2. Crear un usuario administrador `CREATE USER 'AdminCaduca'@'localhost' IDENTIFIED BY 'StKRV6MR6A'; GRANT ALL PRIVILEGES ON caduca.* TO 'AdminCaduca'@'localhost'`
3. Crear un usuario de solo lectura `CREATE USER 'SistemaCaduca'@'localhost' IDENTIFIED BY 'xADcUaP5cs'; GRANT SELECT,INSERT,UPDATE,DELETE ON caltic.* TO 'SistemaCaduca'@'localhost';`

El script completo es:

```sql
CREATE DATABASE caduca CHARACTER SET utf8 COLLATE utf8_general_ci;
CREATE USER 'AdminCaduca'@'localhost' IDENTIFIED BY 'StKRV6MR6A'; 
GRANT ALL PRIVILEGES ON caduca.* TO 'AdminCaduca'@'localhost'
CREATE USER 'SistemaCaduca'@'localhost' IDENTIFIED BY 'xADcUaP5cs'; 
GRANT SELECT,INSERT,UPDATE,DELETE ON caltic.* TO 
'SistemaCaduca'@'localhost';
```

