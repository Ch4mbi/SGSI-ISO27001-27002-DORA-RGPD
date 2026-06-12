# SGSI Aplicado a ChamBank (Banco ficticio)

Sistema de Gestión de Seguridad de la Información (SGSI) diseñado e implantado teóricamente sobre una entidad financiera ficticia, siguiendo los marcos normativos ISO 27001 / ISO 27002, DORA y RGPD

## Descripción del Proyecto

Creación e implantación teórica de un SGSI aplicado a ChamBank, un banco europeo ficticio orientado a servicios financieros digitales. El proyecto cubre desde el contexto organizacional hasta el plan completo de tratamiento de riesgos, pasando por el análisis de activos, identificación de amenazas y la declaración de aplicabilidad (SoA).

El objetivo es demostrar cómo se estructura un SGSI real en el sector financiero, cumpliendo con las principales normativas europeas vigentes.

## Marcos Normativos Aplicados

| Marco | Descripción | 
| --- | --- | 
|ISO 27001 | Marco principal del SGSI. Define los requisitos para gestionar los riesgos de seguridad de la información. | 
| ISO 27002 | Complemento de la ISO 27001 (no certificable). Amplía los controles del Anexo A con guías y buenas prácticas. | 
| DORA | Reglamento europeo de resiliencia operativa digital para el sector financiero. Obligatorio para entidades financieras de la UE. | 
| RGPD | Reglamento General de Protección de Datos. Regula el tratamiento de datos personales de los clientes. | 


## Estructura 

SGSI-ISO27001-27002-DORA-RGPD/

├── [SGSI-ISO-DORA-RGPD.md](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SGSI-ISO-DORA-RGPD.md)      
├── [SoA--SGSI-Ch4mbi.md](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SoA--SGSI-Ch4mbi.md)       
├── README.md                  
└── LICENSE


## Contenido del SGSI

El documento principal SGSI-ISO-DORA-RGPD.md está estructurado siguiendo la lógica de la ISO 27001:

1. Contexto de la organización: Descripción de ChamBank, sus servicios, activos y entorno competitivo.
2. Marco normativo: Justificación y elección de ISO 27001/27002, DORA y RGPD.
3. Términos y definiciones: Glosario específico del proyecto.
4. Liderazgo del SGSI: Roles (CEO, CISO, CTO, CDO, CSO, Pentester) y responsabilidades.
5. Alcance: Sistemas, procesos y personas incluidos y excluidos del SGSI.
6. Planificación: Metodología de análisis de riesgos y objetivos de seguridad.
7. Identificación de activos: Clasificación por tipo y criticidad CIA (Confidencialidad, Integridad, Disponibilidad).
8. Identificación y análisis de riesgos: Análisis cualitativo (mapa de calor) y cuantitativo (VME).
9. Tratamiento de riesgos: Decisiones de mitigación, transferencia o aceptación por cada riesgo.
10. Plan de tratamiento de riesgos: Acciones concretas clasificadas por prioridad y tipo de control.
11. Implantación del SGSI: Recursos necesarios, formación, competencias y concienciación.


La Declaración de Aplicabilidad (SoA) se encuentra en [SoA--SGSI-Ch4mbi.md](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SoA--SGSI-Ch4mbi.md) y recoge los controles de la ISO 27002 seleccionados para ChamBank.

## Organización: ChamBank

ChamBank es un banco europeo digital ficticio que opera en los siguientes ámbitos:

- Bolsa e inversiones: Gestión de carteras digitales y activos financieros.
- Transacciones: Pagos digitales entre particulares y empresas.
- Resguardo de activos: Cuentas bancarias, depósitos y almacenamiento de fondos.
- Seguros: Coberturas frente a robos, accidentes y problemas de salud.
- Préstamos: Financiación con devolución a plazos acordados.

Sus canales principales son una plataforma de banca online, apps móviles, APIs financieras y atención al cliente integrada.

## Metodología deL análisis de riesgos

Se aplica un enfoque mixto (cualitativo + cuantitativo):

- Análisis cualitativo: Mediante mapa de calor (probabilidad × impacto) para riesgos no monetizables directamente (p. ej., reputación).
- Análisis cuantitativo: Mediante el VME (Valor Monetario Esperado = Probabilidad × Impacto financiero estimado) para traducir riesgos a pérdidas esperadas en euros.

El análisis se realiza trimestralmente y tras cada incidente de seguridad significativo. Es gestionado por el CISO y revisado por el comité de dirección.
