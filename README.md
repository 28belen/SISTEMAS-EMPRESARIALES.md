
# PRACTICA 1

#SISTEMAS EMPRESARIALES

|                        |                                                              |                      |                 
| ------                 | ------------------------------------------------------------ |       ----------     | 
| CARRERA:               |                          INGENIERIA DE SISTEMAS              |         Q            | 
| MATERIA:               |                          EMERGENTES II                       |                      | 
| APELLIDOS Y NOMBRES:   |      QUISPE CHAMBI AZUCENA BELEN                             |                      | 
| C.I.:                  |           9932010 L.P.                                       |   INICIAL PATERNO    |  
| LUGAR Y FECHA:         |           LAB-COM 13/08/2019                                 |                      | 


--------------------------------------------------------------------------------------------------------------------


1) Explique que son los sistemas empresariales

      R. Son sistemas que es muy importamnte en el funcionamiento de negociar o de organizar, en caso de que hubiese 
         alguna falla presentara graves consecuencias, este ofrece una alta calidad de servicios que gestiona con grandes
         volumenes de datos, de forma continua que soportara cualquier tipo de organizacion.
         
      

2) Describa cuales son las características más importantes de una aplicación empresarial

       R. -Plataforma tecnológica
          -Alta disponibilidad
          -Escalabilidad
          -Seguridad
          -Mantenimiento


3) Investigue y proponga cinco (5) instituciones que requerirían aplicaciones de misión crítica.
Justifique su respuesta

       R.  - ITC group
           - DEISER
           - BANKIA
           - MAZON WEB SERVICES
           - ATLASSIAN
           
           Se observoque las empresas se están involucrando en la implementación de protocolos que garanticen
           el servicio en el caso de que falle cualquier proceso crítico. Muchas de las soluciones pasan 
           por la virtualización de las aplicaciones de misión crítica y el respaldo dinámico, de manera
           que una base de datos caída sea sustituida de forma inmediata por el backup sin impacto visible
           para el cliente.


4) Explique cuáles son las diferencias entre la escalabilidad horizontal y escalabilidad vertical

       R. -La escalabilidad vertical se refiere a las actualizaciones o modernización de los componentes 
           existentes sin embargo la escalabilidad horzontal se refiere al aumento de numeros descomponentes.


5) Que es un servidor Web y que es un servidor de aplicaciones

       R. - Un servidor web o servidor HTTP es un programa informático que procesa una aplicación del 
            lado del servidor, que realiza conexiones bidireccionales o unidireccionales y síncronas o 
            asíncronas con el cliente y generando o cediendo una respuesta en cualquier lenguaje o Aplicación
            del lado del cliente.
            
          - Servidor de aplicaciones es un servidor en una red de computadores
            que ejecuta ciertas aplicaciones, usualmente se trata de un dispositivo de software que propor-
            ciona servicios de aplicación a las computadoras cliente, un servidor de aplicaciones generalmente
            gestiona la mayor parte (o la totalidad) de las funciones de lógica de negociación y de acceso a 
            los datos de las aplicaciones. Los principales beneficios de la aplicación de la tecnología de 
            servidores de aplicación son la centralización y la disminución de la complejidad en el desarrollo 
            de aplicaciones.
 
6) Con un gráfico explique cómo funciona el protocolo HTTP

        R.

![FUNCIONAMIENTO DEL PROTOCOLO HTTP](http://www.devjoker.com/images/UploadFiles/WindowsLiveWriter/Orden10Fundamentosdefuncionamientodeunaa_FFDC/image_2.png)
       
          - El usuario introduce la url en el navegador
          - El navegador o cliente http decodifica la información obteniendo el esquema o protocolo, la IP o 
            el nombre del servidor web, puerto, etc.
          - El cliente conecta con el servidor web y le solicita la pagina web. Petición HTTP (Request).
          - El servidor envía la pagina web o devuelve el código de error correspondiente. Respuesta HTTP (Response).
          - El navegador o cliente http interpreta los códigos html recibidos y visualiza el resultado.
          - Se cierra la conexión.


7) Explique los elementos importantes de REQUEST en HTTP

        R. - El REQUEST es un pedido que en efecto, la acción de escribir una dirección cualquiera en la línea de URL de 
             tu navegador, se traduce en solicitar un determinado fichero a un servidor, o dicho en la jerga técnica, se le 
             hace un request al servidor. El protocolo que utiliza el navegador (por defecto salvo que se indique otro, como 
             el FTP) para dialogar con un servidor web es el llamado HTTP, que como habrás visto figura al principio de todas 
             las direcciones web. No es necesario escribir el protocolo en los navegadores modernos, simplemente escribimos 
             la dirección de la página solicitada, y el navegador añade delante de la misma su protocolo por defecto. 
             Por ejemplo:
                 sestud.uv.es/manual.esp/ el navegador compone http://sestud.uv.es/manual.esp/

           - El objeto Request permite el acceso a toda la información que pasa desde el navegador del cliente al servidor.
             Al recibir esta información, es repartida y almacenada entre cinco colecciones. Cada colección es similar en 
             estructura a una tabla de datos (también llamada matriz de datos o array). Los datos, una vez cargados, pueden 
             ser accedidos individualmente en cada colección a través de una única clave asignada a cada item, todas las 
             variables pueden ser accedidas directamente mediante una llamada del tipo Request(variable) sin mencionar el 
             nombre de la colección. En este caso, el servidor web busca entre todas las colecciones la clave pedida 
             (variable), buscando por este orden.
             Request.Form("Elemento o indice")[.Count]
           - El contenido de esta colección está formado por todos los elementos de un formulario típico escrito en HTML, 
             donde Elemento es el nombre del elemento del formulario que se quiere recibir desde el navegador (un campo) y 
             Count contiene el número de elementos. En lugar del nombre del elemento, se puede escribir su número de índice, 
             como por ejemplo:
                        -Fichero formulario.htm
                        <HTML><HEAD> <TITLE>Prueba1 ASP</TITLE> </HEAD>
                        <BODY>
                        <FORM ACTION="prueba2.asp" METHOD="POST">
                        Nombre:<INPUT TYPE="text" NAME="Nombre" VALUE="Juan Garcia" ><br>
                        Ciudad:<INPUT TYPE="text" NAME="Ciudad" VALUE="Guadalajara" ><br>
                        Postal:<INPUT TYPE="text" NAME="Postal" VALUE="12345"       ><br>
                        <INPUT TYPE="Submit" VALUE="Enviar">
                        </FORM>
                        </BODY>
                        </HTML>
                -Para poder ver el nombre de los campos y sus contenidos se escribe lo siguiente:
                        -Fichero prueba2.asp
                        <HTML><HEAD> <TITLE>Prueba2 ASP</TITLE> </HEAD>
                        <BODY>
                        Response.Write "Número de elementos: " & Request.Form.Count & "<BR>"
                        Response.Write "Nombre: " & Request.Form("Nombre") & "<BR>"
                        Response.Write "Ciudad: " & Request.Form("Ciudad") & "<BR>"
                        Response.Write "Postal: " & Request.Form("Postal") & "<BR>"
                        Response.Write "<P>"
                        Response.Write "Nombre: " & Request.Form(1) & "<BR>"
                        Response.Write "Ciudad: " & Request.Form(2) & "<BR>"
                        Response.Write "Postal: " & Request.Form(3) & "<BR>"
                        </BODY>
                        </HTML>
 ### El cual nos resulatria:
                        Número de elementos: 3
                        Nombre: Juan Garcia
                        Ciudad: Guadalajara
                        Postal: 12345
                        Nombre: Juan Garcia
                        Ciudad: Guadalajara
                        Postal: 12345




8) Explique los elementos importantes de RESPONSE en HTTP

        R. - Un simple response del servidor web contiene lo siguiente:
             HTTP Status Code (Por ejemplo HTTP/1.1 301 Movido Permanentemente, significa que el recurso requerido 
             fue movido permanentemente y redirigido a otro recurso).
             Encabezados. Igual que en el request, describen el contenido del response (Example – Content-Type: html)
             Una línea vací, un cuerpo de mensaje, que es opcional. Cuando trabajamos con aplicaciones, aquí puede 
             venir la respuesta en XML u otro formato, cuando es una página del navegador, contiene el código HTML 
             que forma nuestra página.
           - Todas las líneas terminan con un retorno de carro y nueva línea. La línea vacía sólo contiene el retorno 
             de carro y la nueva línea sin espacios.
           - No hay mayor ciencia en la comunicación bajo el protocolo HTTP. Pero es poderoso y flexible por que 
             permite desde visualizar páginas web, hasta intercambiar datos entre aplicaciones.


9) Describa con un gráfico la arquitectura Java EE

        R. - Según la definición de Sun, Java Enterprise Edition (Java EE) es el estándar de la industria para 
             desarrollar applicaciones Java portables, rebustas, escalables y seguras en el lado del servidor 
             (server-side). Basado en la solidez de Java SE (Java Standard Edition), Java EE proporciona APIs para
             servicios web, modelo de componetes, gestión y comunicación que hacen lo convierten en el estándar de
             la industria para implementar apliaciones Web y Web 2.0 y aplicaciones con arquitectura orientada a 
             servicios (SOA).
           - Java EE proporciona una arquitectura multi-capa. La capa cliente puede estar constituida por aplicaciones 
             Java de escritorio o navegadores HTML. Las capas proporcionadas por Java EE propiamente dicha son las capas 
             Web (mediante las tecnologías Servlets, JSP y JSF) y las capas de Negocio (mediante tecnologías como EJB, 
             JMS o Web Services). Por último, estas capas se comunican con una capa de datos (base de datos o aplicaciones 
             y sistemas legacy)
             
           
![ARQUITECTURA JAVA EE](http://2.bp.blogspot.com/-Dnnoqh4KDs0/U9-sS6K_faI/AAAAAAAAAOc/s2FPr6g30o8/s1600/Captura.PNG) 
             
             


10) Explique cuáles son los contenedores, componentes y servicios de Java EE

        R. - CONTENEDORES JAVA EE: Escribir aplicaciones empresariales seria muy complejo y difícil de codificar,
             ya que implicaría muchas lineas de código complejo para el manejo de transacciones y la gestión de 
             estados, multihilos y otros detalles de bajo nivel,  la arquitectura Java EE hace que las aplicaciones 
             sean fáciles de escribir porque la lógica de negocio se divide en componentes reutilizables y adicionalmente 
             se cuenta con un servidor de aplicaciones que proporciona servicios en la forma de contenedor para los 
             diferentes tipos de componentes, debido a esto no se tiene que desarrollar estos servicios, sino enfocarse 
             en el desarrollo.
          - SERVICIOS DEL CONTENEDORLos contenedores son la interface entre un componente y el bajo nivel, es 
            especifico para la plataforma, antes de que se pueda ejecutar el componente web, el bean o la aplicación 
            cliente deben ser cargados en un modulo java EE y desplegarlo en el contenedor. al momento de desplegarlo
            cada componente puede tener su propia configuración en cuanto a seguridad, gestión de transacciones JNDI 
            
          - COMPONENTES : Aplicaciones del cliente (Que estan de lado del cliente) , componentes Web (Que esta del lado
            del servidor) y el  componenetes ddel negocio (Que esta del lado del servidor).


11) Investigue los métodos más utilizados de las clases **HttpServlet, HttpServletRequest y
HttpServletResponse** , y para cada uno de los métodos muestre un ejemplo.

         - HttpServlet: public abstract interface Servlet: Todos los servlets implementan este interfaz directamente o 
           extendiendo una clase que lo implemente como HttpServlet. Entre sus métodos están: init(ServletConfig config): 
           Es el método utilizado para crear una nueva instancia del servlet (análogo al constructor).
           
         - HttpServletRequest:Interface que extiende el interface ServletRequest para proporcionar la funcionalidad sobre
           las peticiones HTTP.
           
         - HttpServletResponse: Interface que extiende el interface ServletResponse para proporcionar la funcionalidad de 
           respuesta HTTP.








