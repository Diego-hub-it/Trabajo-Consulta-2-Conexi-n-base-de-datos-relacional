# Trabajo Consulta 2 Conexion base de datos relacional
1. ¿Qué es JDBC y cuáles son sus componentes?
   
   Java Database Connectivity (JDBC) es una especificación API para conectar aplicaciones escritas en Java con datos de bases de datos populares. La API JDBC permite codificar las peticiones de acceso en lenguaje de consulta     estructurado (SQL), que luego se pasan a la aplicación que gestiona la base de datos.
   
   Los componentes de un JDBC son:
   * Driver JDBC: Controladores que permiten la comunicación entre Java y la base de datos.
   * Connection: Interfaz para establecer la conexión con la base de datos.
   * Statement: Utilizado para enviar consultas SQL a la base de datos.
   * ResultSet: Representa los resultados de una consulta SQL. 
2. Documente 2 librerías de Scala que permitan conectarse a una base de datos relacional. En una tabla resuma sus diferencias.
   
   Las librerias mas conocidas en Scala que permitan conectarse a una base de datos relacional son Slick y Doobie.
  
   **SLICK**
  
   Slick es una biblioteca relacional funcional en Scala que facilita el trabajo con bases de datos relacionales. Podemos interactuar con la base de datos casi de la misma manera que lo hacemos con las colecciones de Scala. Además, Slick utiliza programación asincrónica mediante Scala Futures.
    
   Caracteristicas:
   * Abstracción funcional para consultas SQL.
   * Integración con varias bases de datos (MySQL, PostgreSQL, SQLite, etc.).
   * Generación de código para modelos desde el esquema de la base de datos.
   * Soporte para composición de consultas.
   * Gran flexibilidad para escribir consultas dinámicas.
     
   **DOOBIE**
   
   Doobie es una capa JDBC puramente funcional para Scala que permite acceder de manera bajo nivel a características de java.sql. Además, ofrece una API monádica que describe cálculos en diferentes contextos, facilitando la construcción de aplicaciones que interactúan con bases de datos de forma segura y eficiente.

   Caracteristicas:
   * Consultas parametrizadas y dinámicas con inmutabilidad.
   * Basado en la gestión de efectos (cats-effect).
   * Gran control sobre las transacciones.
   * Proporciona pruebas integradas para las consultas SQL.
   * No abstrae SQL: se centra en mantener la escritura directa de las consultas.
   
  | Criterio | Slick | Doobie |
  |----------|-------|--------|
  | Abstracción SQL | Permite usar SQL embebido en Scala como expresiones. | Usa SQL puro directamente, sin abstraer. |
  | Paradigma | Enfoque funcional y orientado a objetos. | Totalmente funcional y basado en cats-effect. |
  | Curva de aprendizaje | Relativamente amigable, con abstracción de SQL. | Más pronunciada debido al enfoque funcional puro. |
  | Transacciones	| Simplificadas con su propia API. | Control explícito sobre transacciones. |
  | Compatibilidad | Compatible con múltiples bases de datos. | Compatible con múltiples bases de datos. |
  | Generación de modelos | Generación automática de modelos desde el esquema. | No genera modelos automáticamente. |
  | Flexibilidad | Alta flexibilidad para consultas dinámicas. | Muy adecuado para desarrolladores que prefieren SQL puro. |
3. Documentar cómo establecer una conexión a una base de datos relacional (mysql). Siga los siguientes pasos:
* Genere una base de datos en mysql
* Genere una tabla con datos de prueba
  
  ![image](https://github.com/user-attachments/assets/948c9a24-c05f-43db-a025-408e77657456)
* Desde Scala establezca la conexión a la base datos

  ![image](https://github.com/user-attachments/assets/726f718c-d5f2-4b66-b5d1-f98e1d9450e7)

* (opcional) Desde Scala realice la consulta de todos los datos de la tabla de prueba.

![image](https://github.com/user-attachments/assets/78558081-a99b-42ea-b08f-90efc7e3f5a4)

Salida de la consulta SQL:

![image](https://github.com/user-attachments/assets/f8552005-fd54-47c4-856b-3c027aeac719)

