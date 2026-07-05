## **11.4. Emergencias** 

Ante situaciones de emergencia por ataques u otros eventos ajenos al banco, se deben de tener planes de reacción y recuperación ante dichos incidentes de emergencia. DORA exige que las entidades financieras tengan “preparados” dichos planes de continuidad del negocio y de recuperación ante incidentes. El protocolo de actuación suele tener los siguientes pasos:

1. **Detección y clasificación**  
   Los responsables de detectar el incidente con un SIEM deben crear una alerta para el equipo de respuesta ante incidentes en base a la severidad del incidente. Es decir, que los trabajadores del SOC deben evaluar la alerta en menos de 30 minutos y que la clasifiquen en base al nivel de severidad de esta.  
2. **Notificación inicial**  
   En caso de que el incidente se considera grave, DORA obliga a notificarlo, aunque no exige tiempos específicos precisos para la notificación, aparte de a el equipo de respuesta ante incidentes, a las respectivas entidades autoritarias, ya que si no se hace puede llevar a sanciones. La notificación inicial se debe llevar a cabo en menos de 4 horas desde que se clasifique como grave, y el resto de los incidentes se deben notificar con un margen de tiempo definido internamente pudiendo ser de 24 horas para las alertas intermedias y varios días para las alertas bajas. Aun así, el RGPD indica que se debe de notificar a los clientes en un plazo máximo de 72 horas.  
3. **Contención**  
   El equipo de respuesta ante incidentes debe de ejecutar las medidas del plan de tratamiento de riesgo, como la segmentación de la red, restauración con backups, desvío de tráfico, etc. Es decir, se debe de reaccionar acorde el playbook específico del incidente en base a sus características. Dicho playbook se debe de elegir una vez identificado el incidente.  
   (Ciberpyme, 2025)  
4. **Recuperación**  
   Se deben activar los planes de continuidad del negocio, como usar servidores de respaldo, restaurar las bases de datos con backups, desviar el tráfico hacia otra infraestructura, etc.  
5. **Informes**  
   El CISO debe de supervisar la elaboración de informes que DORA requiere, y entregarlo en los plazos de tiempo adecuados.

(Álvarez, 2025)  
(España, 2025)  
(Europeo/Consejo, 2026)  
Para emergencias no maliciosas, principalmente formadas por eventos ajenos a la/las compañías, como son apagones, u otros eventos similares, se debe disponer de planes de continuidad operativa (resiliencia). 
