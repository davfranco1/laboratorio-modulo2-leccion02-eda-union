# Laboratorio Módulo 2 Lección 2 EDA Unión

## Estructura de los datos
### Tenemos dos dataframes:
1. El primero contiene id, título, género, premiere, duración, imdb e idioma.
2. El segundo contiene id, tipo, título, director, reparto, país, día añadido, año lanzamiento, rating, duración, listed_in y descripción.
3. De ambos he eliminado la columna "Unnamed: 0" por no aportar valor.
4. En común tenemos el título y la duración.
5. Se han unido las 2 tablas por el elemento común título.

## Algunos findings:
1. La columna duration tiene datos equivocados, por ejemplo, "2 seasons", además, el formato es de tipo string, i.e. "90 min", lo que hace imposible aplicar operaciones matemáticas.
2. Hay 513 títulos originales de Netflix.
3. No se puede determinar si hay diferencias significativas entre la puntuación IMDB de las producciones originales de Netflix y las que no lo son, puesto que no tenemos la puntuación para aquellas que no lo son.
5. El tipo de la fecha debería ser int para poder operar sobre ella. Misma situación con la duración, debería ser int o float.
7. Existen en general muchos valores nulos en el dataframe, incluyendo directores, reparto, países y rating.
8. En la columna duración, hay 425 filas que no corresponden con este dato, sino que es "2 Seasons", que representa un 10% de los datos.
9. En la columna ratings hay 3 valores que se corresponden con la duración, y no el rating, pero son poco relevante porque representan un 0.03% del total.
10. Los tipos más habituales de contenido en Netflix son películas, un 70%, y series de TV, que representan un 30% del total.
11. El 36% del contenido tiene un rating para mayores, y un 25% es apto para menores de 14 años.
12. Los géneros más comunes son: Documentales: 26% y Drama: 14%.
13. El 69% del contenido está en inglés, un 5% en español y otro 5% en hindi.
14. Habiendo 8807 registros únicos del show id, que es el tamaño del dataframe, quiere decir que son válidos como identificadores únicos de cada fila.
15. Hay muchas columnas en las que faltan datos. Particularmente llama la atención la duración, donde falta casi más de la mitad de los registros, siendo un rato importante por ejemplo, para los algoritmos de recomendación al usuario.

## Conclusión
- Sería preciso llevar a cabo una limpieza y completado de los datos para poder alimentar a partir de ellos los algoritmos de recomendación, que son centrales para el modelo de negocio de Netflix, pero requieren información fiable para llevar a cabo su cometido de recomendar contenido relevante al usuario según su idioma, hábitos de uso y preferencias.
- Con información más precisa sería también posible enforcar la creación de contenido al tipo de usuario que se desea captar, considerando su edad, idioma y tipo de contenido (drama, humor, documental...).


