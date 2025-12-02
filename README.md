# NO_SQL_LAB – Fabian Torres

---

##  1. ¿Qué es una base de datos NoSQL y diferencias con SQL?

Una base de datos NoSQL es un sistema no relacional y flexible que permite almacenar datos sin un esquema rígido.  
Diferencias principales frente a SQL:

- No usa tablas fijas.
- Escala horizontal agregando nodos.
- Maneja datos en JSON, documentos, grafos, columnas o key-value.

---

##  2. Rol de MongoDB en el ecosistema NoSQL

MongoDB es una base de datos orientada a documentos (BSON/JSON).  
Es ampliamente usada porque:

- No necesita esquemas estrictos.
- Permite guardar objetos complejos y anidados.
- Es flexible y escalable.
- Tiene agregaciones e índices eficientes.

---

##  3. Base de datos, colección y documento en MongoDB

- **Base de datos:** conjunto de colecciones.  
- **Colección:** conjunto de documentos.  
- **Documento:** registro en formato JSON/BSON.

Ejemplo de documento:
(nombre: Fabian, servicio: Spa, fecha: 2025-12-06, estado: pendiente)

---

##  4. Ventajas del esquema flexible

**Ventajas:**
- Cambios rápidos sin migraciones.
- Adaptable a datos variados.
- Ideal para prototipos.

**Riesgo:**
- Posibles inconsistencias si no se controla bien la estructura.

---

##  5. ¿Qué es Redis?

Redis es un **data structure server**, más que una simple base key-value.  
Maneja estructuras como:

- Strings  
- Hashes  
- Lists  
- Sets  
- Sorted Sets  
- Streams  
- HyperLogLogs  
- Geodatos  

---

##  6. Describir 2 tipos de datos de Redis

### 🔹 Listas (LIST)
- Comandos: LPUSH, RPUSH, LRANGE  
- Uso: colas de tareas, historiales, notificaciones

### 🔹 Sorted Sets (ZSET)
- Comandos: ZADD, ZRANGE  
- Uso: rankings, puntuaciones, prioridades

---

##  7. Laboratorio de turnos

**MongoDB almacena:**
- Usuarios  
- Turnos  
- Horarios  
- Estado de cada turno  

**Redis maneja:**
- Cola de turnos por rapidez  
- Obtener el siguiente turno sin sobrecargar MongoDB  
- Operaciones instantáneas  

---

##  8. Laboratorio del tamagochi

**MongoDB guarda:**
- Datos permanentes del personaje  
- Stats generales  

**Redis maneja:**
- Energía  
- Hambre  
- Temporizadores  
- Valores que cambian muy rápido  

Porque Redis es extremadamente rápido para datos volátiles.

---

##  9. Criterio para mi propia base de datos (reservas)

**MongoDB:**
- Usuarios  
- Reservas  
- Servicios  
- Historial permanente  

**Redis:**
- Caché de disponibilidad  
- Cola de espera  
- TTL para reservas temporales  

---

##  10. Reflexión final

Usaría **MongoDB** para:
- Datos complejos y persistentes  
- Documentos grandes  
- Historial y transacciones  

Usaría **Redis** para:
- Caché  
- Sesiones  
- Rankings  
- Colas rápidas  
- Procesos que deben ser instantáneos  

---

