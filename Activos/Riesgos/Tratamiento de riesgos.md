
# **9. Tratamiento de riesgos** 

Las decisiones de tratamiento de cada riesgo están vinculadas a los objetivos de seguridad de la información, es decir, los puntos mencionados en el apartado 6.2 (Explícito de los objetivos de la seguridad de la información):

* Garantizar la CID   
* Implementación del MFA  
* Detección y respuesta ante incidentes  
* Reducción de incidentes de phishing  
* Cumplimiento normativo DORA, ISO 27001 (con la 27002) y RGPD

De esta manera, en un primer lugar, todas las decisiones para tratar cada riesgo identificado acaban contribuyendo en cierta medida a los objetivos principales de la seguridad de la información introducidos con el SGSI, pudiendo también ser evaluadas en revisiones tras incidentes o auditorías.

* **Datos de clientes**  
  * Phishing🡪Mitigar  
    Cursos de concienciación a los empleados para que en un primer lugar puedan identificar y descartar correos de phishing. Aparte de eso, una medida que revise los correos de entrada al banco, que confirmen si son legítimos o no. Por otro lado, par los clientes se les mandarán correos de concienciación/advertencia.  
  * Robo de datos🡪Mitigar/Transferir  
    Se puede mitigar controlando el acceso (Con diferentes controles de accesos) y aplicando 2FA, aparte de encriptar los datos, filtrar correos con acceso y concienciar a los clientes y empleados.  
* **App de banca online**  
  * Inyecciones sql🡪Mitigar  
    Para poder prevenir dichos ataques lo más recomendable sería quitar todas las entradas permitidas de los usuarios, validar la entrada de datos, aplicar procedimientos correctos y usar consultas parametrizadas (java EE, .net, PHP, …).  
    (Anon., 2025)  
  * Ataques de scripting🡪Mitigar  
    Para mitigar los ataques de scripting, se deben de validar las entradas, llevar a cabo pruebas de penetración para hallar nuevas vulnerabilidades de la misma clase, o revisiones de los datos de entrada en el servidor para confirmar que no son código malicioso.  
    (CLOUDFLARE, 2026)  
  * Puertos desprotegidos🡪Mitigar   
    Se pueden aplicar diferentes medidas de seguridad, como bloquear puertos al menos que den afuera de la red del banco, implementar seguridad de los puertos (port security), y vigilar accesos a los mismos en tiempo real.  
* **Infraestructura cloud**  
  * Accesos no autorizados/Malas autenticaciones🡪Mitigar  
    Revisar en tiempo real los logs para comprobar que no haya comportamiento sospechoso respecto a intentos o ips desconocidas.  
  * Caídas del servicio🡪Transferir/Mitigar  
    Hay que tener un servidor de repuesto o varios para que sustituyan al principal. Por otro lado, hay que tener un equipo de expertos que resuelvan el problema de la caída del servicio.  
* **APIs financieras**  
  * Robo de tokens🡪Mitigar  
    Que los tokens de inicio de sesión sean temporales, que tengan cifrado, y que se tenga una autenticación más segura.  
* **Datos de los empleados**  
  * Robo y manipulación de cuentas profesionales🡪Mitigar  
    Se puede aplicar la MFA, controlar accesos y monitorizar la actividad interna en busca de comportamiento fuera de lugar.  
* **Registros financieros**  
  * Manipulación de datos🡪Mitigar  
    Aplicar backups periódicos para no perder mucha información en caso de alteración, controlar la integridad de los mismos y llevar a cabo auditorias de seguridad.  
* **Servicios internos**  
  * Interrupciones🡪Aceptar/Intentar mitigar  
    Implementar planes de continuidad en el banco, más no se puede hacer ya que es prácticamente inevitable.  
  * Toda clase de ataques internos🡪Mitigar  
    Se pueden controlar, a pesar de ser ciertamente casi inevitables, con equipos de defensa y de respuesta ante incidentes, segmentando la red y monitorizándola.  
* **Servidores**  
  * Ransomware🡪Mitigar  
    Implementar medidas de seguridad como segmentaciones de red (para evitar que se extienda), un EDR, y llevar a cabo backups recurrentes de las bases de datos.  
  * Ddos🡪Mitigar/Transferir  
    Tener otros servidores y/o servicios en la nube para desviar el tráfico no malintencionado y mantener continuidad.  
* **Red interna**  
  * Intrusión🡪Mitigar  
    Se pueden usar firewalls e implementar políticas de seguridad.  
* **Empleados**  
  * Error humano🡪Mitigar  
    Se debe formar a los empleados, implementar políticas de seguridad adecuadas y automatizas procesos críticos.  
* **Clientes**  
  * Fraude🡪Mitigar  
    Implementar sistemas antifraude, reforzar la autenticación de los clientes, e implementar seguros.
