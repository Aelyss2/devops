# Diagrama de Red
El diagrama de red utiliza Route 53 como provisionador de DNS para la conexion afuera de la VPC entre instancias de EC2. Posee 2 balanceadores de cargas que
conectan al usuario con las dos instancias de frontend, como con las instancias de backend. Lo que se busca con los balanceadores es lograr conexiones mas eficientes
al repartir las conexiones entre dos instancias. Ademas el segundo balanceador permite el ruteo con apis externas. El sistema pose dos bases de datos relaciones,
una para almacenar en primera instancia, y la segunda para realizar backup de la primera. Ademas posee una base de datos no relacional con un bucket S3.
Todo el sistema corre en dos instancias distintas de EC2 una para cada zona y ambas conectadas por la misma VPC.
