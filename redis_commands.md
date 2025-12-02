# STRING - Cache de disponibilidad
SET disponibilidad_spa "disponible"
EXPIRE disponibilidad_spa 300

# HASH - Reserva temporal
HSET reserva_temp:1 usuario "Fabian"
HSET reserva_temp:1 servicio "Spa"
HSET reserva_temp:1 fecha "2025-12-06"
EXPIRE reserva_temp:1 120

# LISTA - Cola de reservas urgentes
LPUSH cola_urgentes "Fabian"
LPUSH cola_urgentes "Laura"
LRANGE cola_urgentes 0 -1

# SET - Servicios activos
SADD servicios_activos "Spa"
SADD servicios_activos "Masaje"
SMEMBERS servicios_activos

# SORTED SET - Ranking de clientes por reservas
ZADD ranking_reservas 5 "Fabian"
ZADD ranking_reservas 2 "Laura"
ZRANGE ranking_reservas 0 -1 WITHSCORES
