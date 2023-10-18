# Tipos de Backups

Los backups o copias de seguridad son esenciales para proteger datos ante eventos como fallos técnicos, desastres naturales, errores humanos o ciberataques. Permiten restaurar archivos, bases de datos y sistemas a un estado previo.

Existen varios tipos de backup con diferentes características:

# Backup completo (Full backup)

Realiza una copia de todos los archivos y datos seleccionados para backup. Tiene las siguientes propiedades: 

- Respalda absolutamente todo el conjunto de datos especificado.

- Sirve como punto de restauración independiente, al no requerir de otros backups para recuperar los datos.

- Requiere mayor cantidad de almacenamiento que otros métodos.

- Toma más tiempo para completarse en comparación con backups incrementales o diferenciales.

- Es el punto de partida obligatorio antes de poder realizar otros tipos de backup.

Debido a los amplios tiempos de ejecución y espacio de almacenamiento requerido, los full backups completo no suelen ejecutarse muy frecuentemente, sino periódicamente.

# Backup incremental

Realiza copias sólo de los archivos nuevos o que han cambiado desde el último backup de cualquier tipo. Presenta estas características:

- Respaldan sólo deltas de información. Requieren menor almacenamiento y tiempo de ejecución.

- Para restaurar datos se necesitan el último full backup más todos los incrementales hasta la fecha deseada.

- Si falla o se pierde un incremental, se pierden los cambios contenidos en él.

- Mayor cantidad de backups requeridos para restaurar información.

- No sirven como punto de recuperación independiente. 

Los incrementales suelen programarse con frecuencia, entre los full backups. Optimizan uso de recursos al respaldar sólo diferencias.

# Backup diferencial

Hace copias de los archivos nuevos o modificados desde el último full backup. Sus propiedades:

- Respaldan menos datos que un full pero más que un incremental. Tiempos y espacio intermedios.

- Para restaurar se requiere únicamente el último full backup y el último diferencial. Menos medios que los incrementales.

- Requiere más recursos que los incrementales debido a mayor volumen de datos.

- Si falla, se pierden los cambios desde el último full backup. No sirven de forma independiente.

- El diferencial anterior se invalida al crear uno nuevo.

Los diferenciales ofrecen un equilibrio entre recursos requeridos y facilidad de restauración.

# Backup incremental forever

Variante de los incrementales donde nunca se ejecuta un full backup, sólo se encadenan incrementales recurrentes.

- Optimiza al máximo recursos de almacenamiento y tiempo.

- Complica la recuperación al necesitar una gran cantidad de incrementales.

- Riesgo de pérdida de datos si falla un eslabón de la cadena. 

Adecuado sólo para datos de baja criticidad dada complejidad para restaurar.

# Backup sintético

Un full backup sintético se crea a partir de los datos contenidos en un backup incremental, sin hacer una lectura y copia real de los datos fuente.

- Ahorra tiempo al no acceder a los datos originales.

- Requiere que los incrementales se conserven.

- El resultado es equivalente a un full backup normal.

Útil para crear puntos de recuperación completos periódicamente y mejorar tiempos.

# Backup de registro de transacciones 

Respaldan específicamente los archivos de log o registro de bases de datos y otros sistemas transaccionales.

- Permite recuperar transacciones completadas entre los backups normales. 

- Requiere menos espacio y tiempo que un full backup de toda la base de datos.

- Relevante para bases de datos críticas.

Se suelen programar con mucha frecuencia para reducir pérdida de datos. 

# Backup continuo o CDP

Replica los datos a medida que se producen cambios, creando puntos de recuperación con un RPO muy bajo.

- No es necesario detener la aplicación fuente.

- Requiere menos ancho de banda que sincronización completa.

- Permite recuperación a un punto en el tiempo cercano al incidente.

- Requiere mayor inversión en infraestructura.

Aplica en ambientes de misión crítica con requerimientos de RPO muy bajos.

# Backup de imágenes 

Respaldan una "imagen" completa del estado de un servidor o máquina virtual, incluyendo sistema operativo, aplicaciones, datos, configuraciones, etc.

- Capturan todo el estado del sistema para su restauración.

- Permiten recuperación rápida de un servidor completo.

- Requieren mayor capacidad de almacenamiento.

Muy utilizados para respaldar servidores críticos y configuraciones complejas.

# Copias snapshot

Algunas tecnologías como almacenamiento en redes SAN permiten crear backups tipo snapshot, clonando los datos en un instante determinado, sin interrumpir operaciones.

- No requieren apagar los sistemas fuente. 

- Consumen menos recursos que una copia completa.

- Requieren hardware y software específicos.

- La capacidad de restaurar depende del sistema.

Aprovechan funciones avanzadas de algunas plataformas para backups eficientes.

Cada tipo de backup tiene ventajas y desventajas. Lo recomendable es combinar varios tipos como parte de una estrategia integral de respaldo y recuperación de datos. Esta debe alignarse con los requerimientos de RPO y RTO del negocio. Las pruebas regulares son esenciales para garantizar backups válidos.