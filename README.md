# VO-SOC

![](RackMultipart20211109-4-aetp96_html_f82d96c26cc03594.png)

# **Via Oberta – Servei d&#39;Ocupació de Catalunya**

# **Document d&#39;integració del servei**

 ![](RackMultipart20211109-4-aetp96_html_9b4dd0d250015309.gif) ![](RackMultipart20211109-4-aetp96_html_87fa512ea052536a.gif) ![](RackMultipart20211109-4-aetp96_html_951ed91e1bcd9028.gif) ![](RackMultipart20211109-4-aetp96_html_1eb070f55a9c9a8.gif)

Realitzat per: Unitat de Projectes – Àrea de Tecnologia

Versió: 2.3

Data: 9/11/2021

Arxiu: RackMultipart20211109-4-aetp96.doc

 ![](RackMultipart20211109-4-aetp96_html_e7cf959e7fe4dc1d.png)

**Control del document**

**Informació general**

| **Títol:** | Via Oberta – Servei d&#39;Ocupació de Catalunya. Document d&#39;integració del servei |
| --- | --- |
| **Creat per:** | Unitat de Projectes – Àrea de Tecnologia |
| **A revisar per:** | Unitat de Suport – Àrea de Tecnologia |
| **A aprovar per:** | Unitat de Suport – Àrea de Tecnologia |
| **Llista de distribució:** |
 |
| **Nom del document:** | RackMultipart20211109-4-aetp96.doc |

**Històric de revisions**

| **Versió** | **Data** | **Autor** | **Comentaris** |
| --- | --- | --- | --- |
| V1.0 | 17/01/2009 | Roger Noguera Arnau | Creació del document |
| V2.0 | 08/07/2010 | Roger Noguera Arnau | Incorpora modalitat SOC\_CERT\_DONO |
| V2.1 | 09/08/2012 | Llorenç Camps Vicente | Actualització del joc de proves |
| V2.2 | 09/07/2014 | Llorenç Camps Vicente | Camp Codi SOC obsolet. |
| V2.3 | 12/04/2021 | Roger Noguera Arnau | Baixa de la modalitat SOC\_CERT\_PERCEPTOR. |
|
 |
 |
 |
 |
|
 |
 |
 |
 |

**Índex**

[1Introducció 1](# __RefHeading___ Toc69138263)

[2Transmissions de dades disponibles 1](# __RefHeading___ Toc69138264)

[3Missatgeria dels serveis 1](# __RefHeading___ Toc69138265)

[3.1Certificat d&#39;inscripció del demandant (SOC\_CERT\_INSCRIPCIO) 1](# __RefHeading___ Toc69138266)

[3.1.1Petició – dades específiques 1](# __RefHeading___ Toc69138267)

[3.1.2Resposta – dades específiques 2](# __RefHeading___ Toc69138268)

[3.2Certificat de període d&#39;inscripció (SOC\_CERT\_ULTIMPERIODE) 4](# __RefHeading___ Toc69138269)

[3.2.1Petició – dades específiques 4](# __RefHeading___ Toc69138270)

[3.2.2Resposta – dades específiques 4](# __RefHeading___ Toc69138271)

[3.3Certificat de dades personal (SOC\_CERT\_DADESPERSONALS) 5](# __RefHeading___ Toc69138272)

[3.3.1Petició – dades específiques 5](# __RefHeading___ Toc69138273)

[3.3.2Resposta – dades específiques 6](# __RefHeading___ Toc69138274)

[3.4Certificat de demandant d&#39;ocupació no ocupat (SOC\_CERT\_DONO) 8](# __RefHeading___ Toc69138275)

[3.4.1Petició – dades específiques 8](# __RefHeading___ Toc69138276)

[3.4.2Resposta – dades específiques 8](# __RefHeading___ Toc69138277)

[4Joc de proves 9](# __RefHeading___ Toc69138278)

# 1Introducció

Aquest document detalla la missatgeria associada al servei del Servei d&#39;Ocupació de Catalunya (SOC en endavant).

Per poder realitzar la integració cal conèixer prèviament la següent documentació:

- Document del Servei Via Oberta.
- Document de Missatgeria Genèrica de la PCI del Consorci AOC.

# 2Transmissions de dades disponibles

Les dades disponibles a través del servei són les que es presenten a continuació:

| **EMISSOR** |
| --- |
| SOC (Servei d&#39;Ocupació de Catalunya) |
| **PRODUCTE** | **MODALITAT** | **DESCRIPCIO** |
| **SOC** | SOC\_CERT\_INSCRIPCIO
 | Certificat d&#39;inscripció de demandant d&#39;ocupació.
 |
| --- | --- | --- |
| SOC\_CERT\_ULTIMPERIODE
 | Certificat de períodes d&#39;inscripció.
 |
| SOC\_CERT\_DADESPERSONALS
 | Certificat de dades personals.
 |
| SOC\_CERT\_DONO
 | Certificat de demandant d&#39;ocupació no ocupat.
 |

# 3Missatgeria dels serveis

A continuació es detalla la missatgeria corresponent al bloc de dades específiques de les modalitats de consum del producte SOC.

## 3.1Certificat d&#39;inscripció del demandant (SOC\_CERT\_INSCRIPCIO)

    1.
### Petició – dades específiques

| _Element_ | _Descripció_ |
| --- | --- |
| CertificatRequest/DataIniciSollicitud | Únicament aplica a la modalitat _Certificat d&#39;últim període d&#39;inscripció_ i delimita la data d&#39;inici de la sol·licitud.
 |
| --- | --- |
| CertificatRequest/IdPersona/NIF/TipusDocument | Tipus de document d&#39;identitat (3: NIF, 5: NIE, 6: Ciutadans pertanyents al E.E.E/UE/ confederació Suïssa sense nacionalitat espanyola, que no estan en possessió de NIE, 7: Ciutadans no pertanyents al E.E.E/UE/ confederació Suïssa, amb familiars comunitaris o pertanyents a E.E.E/UE/ confederació Suïssa).
 |
| CertificatRequest/IdPersona/NIF/NumDocument
 | Número de document d&#39;identitat. Format (D: dígit, A: lletra): NIF: DDDDDDDDA, NIE: XDDDDDDDDD, altres: DDDDDDDDA.
 |
| CertificatRequest/PerCod
 | _ **Camp obsolet** _. Identificació del demandant mitjançant el codi intern de la plataforma del SOC. En cas d&#39;informar aquest codi, no es requereix informar el bloc de dades NIF.
 |

![](RackMultipart20211109-4-aetp96_html_bf3ef3bdf85077c6.gif)

    1.
### Resposta – dades específiques

| _Element_ | _Descripció_ |
| --- | --- |
| CertInscripcioResponse/CertificatRequest | Dades de la petició. Vegeu apartat Error: Reference source not found.
 |
| --- | --- |
| CertInscripcioResponse/DataProces | Data de processament de la petició per part de la plataforma del SOC.
 |
| CertInscripcioResponse/DadesComunes | Dades del titular informat en la petició. Vegeu apartat Error: Reference source not found.
 |
| CertInscripcioResponse/CertInscripció/DemandantInscrit | Indicador de si el titular està inscrit (S | N).
 |
| CertPerceptorResponse/PICAError | Detalls de l&#39;incidència en cas d&#39;error processant la petició. Vegeu apartat Error: Reference source not found.
 |

![](RackMultipart20211109-4-aetp96_html_eb0dc3ec6078d0ce.gif)

#### 3.1..1Dades comunes

| _Element_ | _Descripció_ |
| --- | --- |
| //DadesComunes/NIF/TipusDocument | D: persones amb nacionalitat espanyola en possessió de DNI, E: persones sense nacionalitat espanyola en possessió de NIE, U: ciutadans pertanyents al E.E.E/UE/ confederació Suïssa sense nacionalitat espanyola que no estan en possessió de NIE., W: Ciutadans no pertanyents al E.E.E/UE/ confederació Suïssa amb familiars comunitaris o pertanyents a E.E.E/UE/ confederació Suïssa. |
| --- | --- |
| //DadesComunes/NIF/DescTipusDocument | Descripció del tipus de document d&#39;identitat.
 |
| //DadesComunes/NIF/NumDocument | Número de document d&#39;identitat.
 |
| //DadesComunes/NIF/LletraDocument | Lletra del NIF.
 |
| //DadesComunes/PerCod
 | _ **Camp obsolet** _. Codi intern de la plataforma del SOC que identifica el demandant. |
| //DadesComunes/Nom
 | Nom del demandant. |
| //DadesComunes/Cognom1
 | Primer cognom del demandant. |
| //DadesComunes/Cognom2
 | Segon cognom del demandant. |
| //DadesComunes/Nacionalitat
 | Codi de la nacionalitat del demandant. |
| //DadesComunes/DescNacionalitat
 | Descripció de la nacionalitat del demandant. |
| //DadesComunes/Sexe
 | Codi de sexe del demandant (1, 2). |
| //DadesComunes/DescSexe
 | Descripció del sexe del demandant (1, 2). |
| //DadesComunes/DataNaixement
 | Data de naixement del demandant. |

#### 3.1..2Dades d&#39;error

| _Element_ | _Descripció_ |
| --- | --- |
| //PICAError/CodiError | Codi d&#39;error.
 |
| --- | --- |
| //PICAError/Error | Literal o excepció associada a l&#39;error.
 |
| //PICAError/Descripcio | Descripció de l&#39;error.
 |
| //PICAError/Causa | Traça de detall de l&#39;error.
 |

## 3.2Certificat de període d&#39;inscripció (SOC\_CERT\_ULTIMPERIODE)

    1.
### Petició – dades específiques

El format de la petició és identic al detallat a l&#39;apartat Error: Reference source not found.

    1.
### Resposta – dades específiques

| _Element_ | _Descripció_ |
| --- | --- |
| CertUltimPeriodeResponse/CertificatRequest | Dades de la petició. Vegeu apartat Error: Reference source not found.
 |
| --- | --- |
| CertUltimPeriodeResponse/DataProces | Data de processament de la petició per part de la plataforma del SOC.
 |
| CertUltimPeriodeResponse/DadesComunes | Dades del titular informat en la petició. Vegeu apartat Error: Reference source not found.
 |
| CertUltimPeriodeResponse/CertInscripció/NumDiesInscrit | Nombre de dies que consta que la persona està inscrita com a demandant d&#39;ocupació des de la data d&#39;inici de la sol·licitud. |
| CertUltimPeriodeResponse/PeriodeIns/IniciPeriode
 | Data d&#39;inici del període. |
| CertUltimPeriodeResponse/PeriodeIns/FiPeriode
 | Data de finalització del període. |
| CertUltimPeriodeResponse/PICAError | Detalls de l&#39;incidència en cas d&#39;error processant la petició. Vegeu apartat Error: Reference source not found.
 |

![](RackMultipart20211109-4-aetp96_html_a44a88713df922af.gif)

## 3.3Certificat de dades personal (SOC\_CERT\_DADESPERSONALS)

    1.
### Petició – dades específiques

El format de la petició és identic al detallat a l&#39;apartat Error: Reference source not found.

    1.
### Resposta – dades específiques

![](RackMultipart20211109-4-aetp96_html_38f6f00f6a514430.gif)

| _Element_ | _Descripció_ |
| --- | --- |
| CertDadesPersonalsResponse/CertificatRequest | Dades de la petició. Vegeu apartat Error: Reference source not found.
 |
| --- | --- |
| CertDadesPersonalsResponse/DataProces | Data de processament de la petició per part de la plataforma del SOC.
 |
| CertDadesPersonalsResponse/DadesComunes | Dades del titular informat en la petició. Vegeu apartat Error: Reference source not found.
 |
| CertDadesPersonalsResponse/CertDadesPersonals/PaisResidencia | Codi de país de residència. |
| CertDadesPersonalsResponse/CertDadesPersonals/DescPaisResidencia | Descripció de país de residència. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/TipusVia | Codi de tipus de via. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescVia | Descripció de tipus de via. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/NomVia | Nom de via. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/NumVia | Número de la via. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/BisDup | Bis / duplicat de l&#39;escala. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescBisDup | Descripció bis / duplicat de l&#39;escala. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Escala | Escala. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Pis | Pis. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/LletraNum | Lletra. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Provincia | Codi de província. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescProvincia | Descripció de província. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Illa | Codi d&#39;illa. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescIlla | Descripció d&#39;illa. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Municipi | Codi de municipi. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescMunicipi | Descripció de municipi. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/Localitat | Codi de localitat. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescLocalitat | Descripció de localitat. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/CodiPostal | Codi postal. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/EntitatSingular | Codi d&#39;entital singular, |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEspanya/DescEntitatSingular | Descripció d&#39;entital singular, |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEstranger/DomiciliEstranger1 | Domicili estranger 1. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEstranger/DomiciliEstranger2 | Domicili estranger 2. |
| CertDadesPersonalsResponse/CertDadesPersonals/DadesResidencia/DomiciliEstranger/CodiPostalEstranger | Codi de domicili estranger. |
| CertDadesPersonalsResponse/PICAError | Detalls de l&#39;incidència en cas d&#39;error processant la petició. Vegeu apartat Error: Reference source not found.
 |

## 3.4Certificat de demandant d&#39;ocupació no ocupat (SOC\_CERT\_DONO)

    1.
### Petició – dades específiques

El format de la petició és identic al detallat a l&#39;apartat Error: Reference source not found.

    1.
### Resposta – dades específiques

| _Element_ | _Descripció_ |
| --- | --- |
| CertDonoResponse/CertificatRequest | Dades de la petició. Vegeu apartat Error: Reference source not found.
 |
| --- | --- |
| CertDonoResponse/DataProces | Data de processament de la petició per part de la plataforma del SOC.
 |
| CertDonoResponse/CertDono/Demanda | Bloc amb les dades de la demanda.
 |
| //Demanda/IndDono | Indicador de si la demanada és DONO (S, N).
 |
| //Demanda/DataDono | Data en la que s&#39;ha calculat si la demanda és DONO.
 |
| CertDonoResponse/CertDono/PersonaFisica | Bloc amb les dades de la persona.
 |
| //PersonaFisica/NIF/TipusDocument | D: persones amb nacionalitat espanyola en possessió de DNI, E: persones sense nacionalitat espanyola en possessió de NIE, U: ciutadans pertanyents al E.E.E/UE/ confederació Suïssa sense nacionalitat espanyola que no estan en possessió de NIE., W: Ciutadans no pertanyents al E.E.E/UE/ confederació Suïssa amb familiars comunitaris o pertanyents a E.E.E/UE/ confederació Suïssa.
 |
| //PersonaFisica/NIF/DescTipusDocument | Descripció del tipus de document d&#39;identitat.
 |
| //PersonaFisica/NIF/NumDocument | Número de document d&#39;identitat.
 |
| //PersonaFisica/NIF/LletraDocument | Lletra del NIF.
 |
| //PersonaFisica/PerCod | _ **Camp obsolet.** _ Codi intern de la plataforma del SOC que identifica el demandant.
 |
| //PersonaFisica/Nom | Nom del demandant.
 |
| //PersonaFisica/Cognom1 | Primer cognom del demandant.
 |
| //PersonaFisica/Cognom2 | Segon cognom del demandant.
 |
| //PersonaFisica/PaisResidencia | Codi de pais de residència.
 |
| //PersonaFisica/DescPaisResidencia | Descripció del país de residència.
 |
| CertDonoResponse/PICAError | Detalls de l&#39;incidència en cas d&#39;error processant la petició. Vegeu apartat Error: Reference source not found.
 |

![](RackMultipart20211109-4-aetp96_html_a25b48b58e7897c0.gif)

# 4Joc de proves

L&#39;emissor final publica els següent joc de proves a l&#39;entorn de pre-producció:

| _Descripció_ | _DNI_ | _Codi SOC_ | _Data_ |
| --- | --- | --- | --- |
| DNI correcte | 35011089Y |
 |
 |
| Codi SOC correcte |
 | 4786899 |
 |
| NIE correcte | Y0021937D |
 |
 |
| Codi SOC correcte |
 | 5836366 |
 |
| DNI i data correcte | 35011089Y |
 | 01012001 |
| Codi SOC i data correcte |
 | 4786899 | 01012001 |
| Ciutadants pertanyents a la UE correcte | 07079263R |
 |
 |
| Codi SOC correcte |
 | 5197189 |
 |
| DNI no existent | 11111111H |
 |
 |
| DNI de baixa | 43711548W |
 |
 |
| Codi SOC incorrecte |
 | 4503158 |
 |