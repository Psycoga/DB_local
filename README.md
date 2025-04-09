### Bases de datos en local

- Vamos a utilizar el siguiente comando para buscar bases de datos en el sistema:
```bash
find / -type f \( -name "*.db" -o -name "*.sql" -o -name "*.sqlite" \) 2>/dev/null
```

- Para abrir una base de datos SQLite, usamos el siguiente comando:
```bash
sqlite3 /path/to/database.db
```

- Por ejemplo, para abrir la base de datos `gophish.db`:
```bash
sqlite3 /var/lib/gophish/gophish.db
```

#### Ver las tablas disponibles
Para listar todas las tablas de la base de datos, usamos:
```bash
sqlite> .tables
```
![alt text](/ANEXOS/image-1.png)

#### Ver el contenido de una tabla
Por ejemplo, si la tabla se llama `users`, el comando sería:
```bash
sqlite> SELECT * FROM users;
```

Esto mostrará todas las filas y columnas de la tabla.

![alt text](/ANEXOS/image-2.png)

#### Ver el esquema de una tabla
Para ver cómo está definida una tabla (su estructura), usamos:
```bash
sqlite> .schema;
```
Esto mostrará el esquema de todas las tablas.
![alt text](/ANEXOS/image-3.png)

### Resumen del proceso
1. Busca bases de datos en tu sistema con `find`.
2. Abre la base de datos con `sqlite3`.
3. Usa `.tables` para listar las tablas.
4. Usa `SELECT * FROM nombre_tabla;` para ver el contenido de una tabla.
5. Usa `.schema ` para ver la estructura de las tabla.
