Guía de Uso del Paquete dplyr en R
Bienvenido a la guía de uso del paquete dplyr en R. Esta guía está diseñada para ayudarte a comprender y utilizar eficientemente las funciones que dplyr ofrece para el procesamiento y manipulación de datos.
Introducción
dplyr es un paquete del ecosistema tidyverse que proporciona un conjunto de funciones intuitivas y eficientes para manipular datos en R. Facilita tareas comunes como filtrar filas, seleccionar columnas, reordenar datos y resumir información.
Instalación
Para instalar y cargar dplyr, puedes usar los siguientes comandos en R:

r
Copiar
Editar
install.packages("dplyr")  # Instalación desde CRAN
library(dplyr)             # Carga del paquete
Funcionalidades Principales
A continuación, se describen algunas de las funciones más utilizadas de dplyr:

filter(): Filtra filas según condiciones específicas.
select(): Selecciona columnas por sus nombres.
mutate(): Crea o modifica columnas existentes.
arrange(): Ordena las filas según una o más columnas.
summarise(): Resume múltiples valores en un solo valor.
group_by(): Agrupa los datos para operaciones posteriores.
Ejemplos de Uso
A continuación, se presentan ejemplos básicos de cómo utilizar algunas de las funciones de dplyr:

r
Copiar
Editar
# Cargar el paquete
library(dplyr)

# Crear un data frame de ejemplo
datos <- data.frame(
  nombre = c("Ana", "Luis", "María", "Juan"),
  edad = c(23, 30, 22, 25),
  puntaje = c(85, 90, 88, 92)
)

# Filtrar filas donde la edad es mayor a 24
datos_filtrados <- filter(datos, edad > 24)

# Seleccionar las columnas nombre y puntaje
datos_seleccionados <- select(datos, nombre, puntaje)

# Crear una nueva columna que es el doble del puntaje
datos_mutados <- mutate(datos, puntaje_doble = puntaje * 2)

# Ordenar los datos por puntaje de manera descendente
datos_ordenados <- arrange(datos, desc(puntaje))

# Calcular el puntaje promedio
puntaje_promedio <- summarise(datos, promedio = mean(puntaje))
Recursos Adicionales
Para profundizar en el uso de dplyr, se recomiendan los siguientes recursos:

Documentación oficial de dplyr
Libro "R para Ciencia de Datos" por Hadley Wickham & Garrett Grolemund