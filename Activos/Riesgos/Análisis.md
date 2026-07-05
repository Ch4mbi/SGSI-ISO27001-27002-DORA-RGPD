
## **8.2. Análisis de los riesgos**

Como ya se mencionó, el análisis de riesgos se conforma de dos estructuras: primero una valoración cualitativa con la que, por medio de un mapa de calor, permite identificar los riesgos cuando el impacto no es, directamente, monetizable, después, se lleva a cabo una valoración cuantitativa con el VME (Valor monetario esperado) que traduce los riesgos a una pérdida financiera esperada, permitiendo que ChamBank pueda comparar el coste del riesgo con el coste de mitigación del mismo permitiendo tomar decisiones financieras.  
(Team, 2025)

### **8.2.1. Análisis cualitativo** 

Las estimaciones y conclusiones se van a sacar en base a esta tabla:

|  | Muy poco probable | Poco probable | Probable (Medio) | Muy probable | Extremadamente probable |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Impacto fatal** | Alto | Alto | Alto | Alto | Alto |
| **Impacto considerable** | Medio | Medio | Alto | Alto | Alto |
| **Impacto moderado** | Medio | Medio | Medio | Medio | Medio |
| **Impacto bajo** | Bajo | Bajo | Medio | Medio | Medio |
| **Impacto insignificante** | Bajo | Bajo | Bajo | Bajo | Bajo |

(Team, 2025)  
(Enrique, 2026)

### **8.2.2. Análisis cuantitativo** 

Para los riesgos con un impacto económico posiblemente medible, en ChamBank se ha decidido aplicar el valor monetario esperado (VME= Probabilidad * impacto financiero estimado). Este método se elige dobre alternativas como FMEA o BIA ya que ChamBank, en esta fase inicial en la que se encuentra, necesita una métrica simple que permita a la dirección del banco comparar riesgos respecto a pérdidas esperadas y priorizar la inversión en controles. Los parámetros que se han usado son:

| Probabilidad                                                                                           | Impacto                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| Muy poco probable🡪10% Poco probable🡪25% Probable🡪50% Muy probable🡪75% Extremadamente probable🡪90% | Insignificante🡪<=10000€ Bajo🡪50000€ Moderado🡪50000-150000€ Considerable🡪>=750000€ Fatal🡪>2000000€ |

(Team, 2025)  
(alvarez, 2024)

## **8.3. Tabla de análisis** 

| Grupo | Riesgo | Análisis cualitativo | Análisis cuantitativo | Justificación |
| :---: | :---: | ----- | ----- | ----- |
|  **Datos de clientes** |  Phishing | **Probabilidad**: Muy probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:75% **Impacto**: 750000€ **VME**: 0,75*750000=  562500€ | Es uno de los métodos de ataque más usados principalmente por la ignorancia de los clientes (en gran medida), por lo que su probabilidad de que pase es muy alta, y el impacto es considerable debido a los datos que aporta a los atacantes. |
|  **Datos de clientes** |  Robo de datos | **Probabilidad**: Probable **Impacto**: Considerable-fatal **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 2000000€ **VME**: 0.5*2000000= 1000000€ | Es una consecuencia de un ataque exitoso en el banco. Por lo que es probable que ocurra (no muy probable ya que hay equipos de defensa o IR) y el impacto potencial que puede tener puede llegar a ser fatal. |
|  **App banca online** |  Inyecciones sql | **Probabilidad**: Probable **Impacto**: Fatal **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 2000000€ **VME**: 0.5*2000000= 1000000€ | El riesgo es probable ya que hay que tener en cuenta que hoy en día no son tan efectivas como lo fueron al principio, existen medidas de seguridad que se deben implementar en un primer lugar, aunque el impacto potencial es fatal, ya que pueden alterar datos de diversas maneras con dichas inyecciones. |
|  **App banca online** |  Scripting | **Probabilidad**: Probable **Impacto**: Considerable-fatal **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 1500000€ **VME**: 0,5*1500000=  750000€ | En aplicaciones web son vulnerabilidades que se suelen repetir, por lo que es probable que ocurra, y permiten ejecutar código malicioso, por lo que pueden llegar a tener un impacto considerable o fatal. |
|  **App banca online** |  Puertos desprotegidos | **Probabilidad**: Poco probable **Impacto**: Fatal **Riesgo**: Alto | **Probabilidad**:25% **Impacto**: 2000000€ **VME**: 0,25*200000= 500000€  | Aunque son menos frecuentes que otros, el hecho de que da acceso a los atacantes a servicios internos lo pone en un impacto alto, por lo que es un riesgo alto. |
|  **Infraestructura cloud** |  Accesos no autorizados | **Probabilidad**: Probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 750000€ **VME**: 0,5*750000=  375000€ | Una nube con seguridad mal configurada permite accesos no autorizados a datos o recursos, afectando a su confidencialidad. |
|  **Infraestructura cloud** |  Caídas del servicio | **Probabilidad**: Probable **Impacto**: Moderado- Considerable **Riesgo**: Medio-Alto | **Probabilidad**:50% **Impacto**: 400000€ **VME**: 0,5*400000=  200000€ | Ya que puede deberse a fallos internos o a ataques, es un problema habitual, su impacto depende de la resiliencia del banco y/o de la capacidad de recuperación del mismo. |
|  **APIs financieras** |  Robo de tokens | **Probabilidad**: Probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 750000€ **VME**: 0,5*750000=  375000€ | Es un riesgo considerable por el posible robo de credenciales de acceso, permitiendo así suplantar la identidad de clientes o empleados con diversos fines, por eso tiene un impacto considerable.  |
|  **Datos de los empleados** |  Robo/ Manipulación de cuentas profesionales | **Probabilidad**: Probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 750000€ **VME**: 0,5*750000=  375000€ | El acceso a cuentas internas es probable ya que existen equipos especializados en la defensa de las cuentas, pero si llegan a penetrar los atacantes, el impacto que tiene será alto. |
| **Registros financieros** |  Manipulación de datos | **Probabilidad**: Poco probable **Impacto**: Fatal **Riesgo**: Alto | **Probabilidad**:25% **Impacto**: 2000000€ **VME**: 0,25*200000= 500000€ | Por los controles es menos probable que pase, pero si llegase a pasar, su impacto sería crítico ya que afecta a la integridad de los datos y puede llevar, aparte del ataque en sí, a consecuencias legales y sanciones. |
|  **Servicios internos** |  Interrupciones | **Probabilidad**: Probable **Impacto**: Moderado **Riesgo**: Medio | **Probabilidad**:50% **Impacto**: 100000€ **VME**: 0,5*100000=  50000€ | Afectan a la operativa interna y pueden ser por causas “naturales” (Apagones, por ejemplo) o intencionados, como ataques de denegación de servicios que afecten a la funcionalidad normal del sistema. |
|  **Servicios internos** |  Ataques internos (En general) | **Probabilidad**: Probable **Impacto**: Fatal **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 2000000€ **VME**: 0,5*2000000= 1000000€  | Ya que dependen de los propios ataques, son probables a que pasen, ya que un equipo de profesionales puede bloquear una mayoría de ellos, pero es posible que alguno pase desapercibido. Una vez dentro, pueden llevar a cabo diversas acciones causando así que el impacto potencial pueda llegar a ser fatal. |
|  **Servidores** |  Ransomware | **Probabilidad**: Probable **Impacto**: Fatal **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 2000000€ **VME**: 0,5*750000= 375000€ | Es una de las amenazas más grandes en toda clase de entornos, incluyendo el financiero, ya que pueden paralizar los sistemas y/o cifrar grandes volúmenes de datos. |
|  **Servidores** |  Ddos | **Probabilidad**: Probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 750000€ **VME**: 0,5*750000= 375000€ | Son ataques que afectan a la disponibilidad de los servicios, son probables a que pasen hoy en día, y su impacto es considerable dependiendo del tiempo de respuesta ante dicho ataque. |
|  **Red interna** |  Intrusión | **Probabilidad**: Probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:50% **Impacto**: 750000€ **VME**: 0,5*750000=  375000€ | La intrusión a la red puede permitir el acceso a sistemas internos y facilitar auques como movimientos laterales. |
|  **Empleados** |  Error humano | **Probabilidad**: Probable **Impacto**: Moderado- Considerable **Riesgo**: Medio | **Probabilidad**:50% **Impacto**: 200000€ **VME**: 0,5*200000= 100000€ | Una parte de los ataques se producen gracias al error humano, por lo que es relativamente probable que ocurran, aunque su impacto puede variar dependiendo de la víctima. |
|  **Empleados** |  Dispositivos externos | **Probabilidad**: Probable **Impacto**: Moderado **Riesgo**: Medio | **Probabilidad**:50% **Impacto**: 100000€ **VME**: 0,5*100000= 50000€ | El uso de dispositivos personales puede introducir en el banco malware, aunque el impacto puede controlarse. |
|  **Clientes** |  Fraude | **Probabilidad**: Muy probable **Impacto**: Considerable **Riesgo**: Alto | **Probabilidad**:75% **Impacto**: 750000€ **VME**: 0,75*750000= 562500€ | Es una de las amenazas más frecuente al sector bancario, con un gran impacto reputacionales y/o económicos. |

A partir de los resultados obtenidos, se pueden priorizar riesgos en función de su impacto económico esperado, y estimaciones funcionales, permitiendo al banco enfocar sus recursos en los riesgos que supondrían una perdida potencial mayor, y que se deben abordar de manera inmediata, los cuales serían:

* Robo de datos  
* Ataques internos   
* Ransomware

Estos aspectos son los más relevantes a nivel cuantitativo y que conviene cubrir y tener planes para responder ante ellos.   
Por otro lado, hay riesgos que se deben abordar, pero no inmediatamente, que se deben de ir abordando, pero no con prioridad absoluta como:

* Phishing  
* Scripting  
* Puertos desprotegidos  
* Accesos no autorizados  
* Tokens  
* Caídas del servicio  
* Manipulación de datos  
* Denegación de servicios  
* Intrusiones

También hay otros que son “asumibles” por el banco como:

* Interrupciones  
* Dispositivos externos  
* Errores humanos

Cabe destacar que los riesgos de seguridad están vinculados con los objetivos de seguridad que ChamBank se propusieron alineados con los objetivos de la implantación del SGSI. El robo de datos y los ataques internos conforman ataques que afectan tanto a la confidencialidad y a la integridad, ya que una filtración lo incumpliría. Por otro lado, el ransomware, amenazaría a la disponibilidad, afectando a los servicios internos que ofrece el banco a los clientes. O los ataques de phishing, que, a pesar de tener como objetivo reducirlos, sigue siendo una amenaza persistente que, de hecho, puede dar lugar a otros ataques ya mencionados. La alineación mencionada permite que el plan de tratamiento de riesgos sirva como herramienta extra para cumplir los compromisos que requiere la implantación del SGSI.
