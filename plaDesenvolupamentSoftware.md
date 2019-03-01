# SISTEMA SocMus - PLA DE DESENVOLUPAMENT DE SOFTWARE #

## 1. ORGANITZACIÓ I EQUIP ##

- Cap de Projecte (1 Persona): Ha de planificar i programar el projecte, descompondre-ho en tasques i assignar-les als membres de l'equip. Ha de supervisar, liderar i coordinar l'equip, veure que tots els membres de l'equip estan realitzant les tasques que se'ls ha encarregat.

- Analista Sènior (1 Persona): És l'encarregat del desenvolupament d'aplicacions en el camp del disseny i orientació dels algorismes, així com d'analitzar les possibles utilitats i modificacions necessàries dels sistemes operatius per una major eficiència d'un sistema informàtic. Una altra missió que tenen és donar suport tècnic als usuaris de l'aplicació.

- Arquitecte del Software (1 Persona): És l'encarregat d'analitzar els requisits que influeixen en l'arquitectura i fer-ne un disseny arquitectònic. Estructura, defineix el funcionament i interacció entre les parts de tot software (bases de dades, servidor, webs).

- Dissenyador Gràfic (1 Persona): És el responsable de dissenyar tota la interfície gràfica d'usuari i de distribuir les funcionalitats en l'aplicació.

- Programadors Front-end (2 Persones): Són els encarregats de programar la Capa de Presentació i d'implementar la lògica de la web que es connecta amb el servidor.

- Programadors Back-end (2 Persones): Són els encarregats de muntar el servidor perquè aquest pugui rebre les peticions de les webs que han programat el front-end i manegen les dades, comunicant-se amb la base de dades quan es necessita informació i tornant-li tota la informació que necessiten les webs.

- Programadors júniors (2 Persones): Són els programadors amb menys experiència. S'encarreguen de fer les tasques encarregades pels sèniors i així guanyar coneixements i experiència.

- Tester (1 Persona): És el responsable de dur a terme proves preestablertes a l'aplicació abans del seu llançament al mercat per tal de garantir la qualitat, la integritat del disseny i el funcionament correcte d'aquesta.


## 2. PLA DE PROJECTE ##

### 2.1. Estimació d'esforç ###

![Imgur](http://i.imgur.com/1mPj5fl.png)

![Imgur](http://i.imgur.com/PQTpT0Q.png)

Motiu d'assignació de pesos:

- Estudiant (pes 1): S'assigna el pes 1 perquè és una superclasse però qui interactua realment són les subclasses d'aquesta superclasse, per tant no tindrà pes, ja que únicament és un actor passatger.

- Estudiant Erasmus (pes 3): Apareix la interacció humana per part dels estudiants que vénen d'Erasmus i estan registrats com usuari.

- Estudiant Local (pes 3): Apareix la interacció humana dels estudiants locals registrats com usuari.

- Google Calendar (pes 1): És una aplicació externa, ja programada, que s'utilitza com a camí per facilitar la funcionalitat i la programació de la mateixa aplicació, en aquest cas, s'usa per als esdeveniments.

- Google Drive (pes 1): És una aplicació externa, ja programada, que s'utilitza com a camí per facilitar la funcionalitat i la programació de la nostra aplicació, en aquest cas, sobretot en aquest cas s'usa per compartir imatges.

![Imgur](http://i.imgur.com/xFzp8pV.png)

![Imgur](http://i.imgur.com/D4EUuJ1.png)

Motiu d'assignació de pesos:

- Registrar-se (pes 5): Per la funció de registrar a un usuari s'usaran 2 esdeveniments:
1. Introduir les dades a la Base de Dades
2. Entrar a l'aplicació, carregant-ne la imatge.

- Gestionar Dades (pes 5): Per gestionar les dades com a màxim usarem 2 esdeveniments:
1. Introduir les noves dades.
2. Fer el canvi a la Base de Dades.

- Enviar Sol·licitud (pes 10): Per enviar una sol·licitud es realitzaran 4 esdeveniments:
1. Obrir el cercador.
2. Buscar a l'usuari en concret. (apareix una llista dels possibles usuaris demanats)
3. Mostrar el perfil de l'usuari demanat
4. Enviar la sol·licitud, fent saltar una notificació a l'altre usuari.

- Acceptar Sol·licitud (pes 5): Per acceptar una sol·licitud es realitzaran 2 esdeveniments:
1. Veure el perfil de la persona sol·licitant.
2. Acceptar, clicant al botó d'acceptar.

- Rebutjar Sol·licitud (pes 5): Per rebutjar una sol·licitud es realitzaran 2 esdeveniments:
1. Veure el perfil de la persona sol·licitant.
2. Rebutjar, clicant al botó de rebutjar.

- Crear Esdeveniments Oberts / Tancats (pes 15): Els esdeveniments oberts i tancats seguiran el mateix patró de creació: Per crear un esdeveniment es realitzaran 8 esdeveniments:
1. Seleccionarà el tipus d'esdeveniment
2. Posarà un nom a l'esdeveniment.
3. Sortirà un calendari, a través de Google calendar.
4. Seleccionarà una data.
5. La data s'establirà com a data de l'esdeveniment si l'empresa o el lloc on es fa l'esdeveniment ha informat amb anterioritat de la disponibilitat en aquella data.
6. S'omplirà un formulari bàsic amb les dades de l'esdeveniment.
7. Es crearà l'esdeveniment.
8. Es crearà el xat per defecte d'aquest esdeveniment.

- Unir-se a un Esdeveniment (pes 10): Per afegir-se a un esdeveniment es realitzaran 4 esdeveniments:
1. Selecciona l'esdeveniment en el qual es vol participar i surt per pantalla la informació d'aquest
2. Selecciona l'opció d'afegir-se
3. Treu per pantalla un missatge on s'informa de si l'usuari ja està inscrit per l'esdeveniment i si l'esdeveniment està complet.
4. Demana si vol un missatge per si algun usuari cancel·la la seva participació, en aquest cas es farà un darrer esdeveniment on es guardarà a una llista les dades de l'usuari per si hi ha una plaça lliure, notificar-li.

- Cancel·lar assistència a un Esdeveniment (pes 10): Per cancel·lar l'assistència a un esdeveniment es realitzaran 4 esdeveniments:
1. Entrar a la llista d'esdeveniments on està assegurada la participació.
2. Selecciona l'esdeveniment que es vol cancel·lar i es clica al botó de cancel·lar participació.
3. Apareixerà una finestra on es preguntarà si està segur.
4. Si hi ha algú pendent a la llista d'espera d'aquell esdeveniment, se li enviarà una notificació per si es vol inscriure.

- Compartir Imatges (pes 10): Per compartir imatges d'un esdeveniment passat es realitzaran 5 esdeveniments:
1. Entrar a l'esdeveniment en qüestió.
2. Selecciona l'opció de compartir imatges, aquesta opció et redirigeix a Google Drive.
3. Es penjaran les fotografies a una carpeta de Google Drive ja creada i compartida amb tots els usuaris que han participat en l'esdeveniment.
4. Un cop posades totes les fotografies, tornem a l'aplicació de SocMus
5. Acceptem la transacció per compartir des de la nostra aplicació l'enllaç de les fotografies penjades.

- Personalitzar Xat (pes 5): Per personalitzar un xat es realitzaran 3 esdeveniments:
1. Accedir a la pantalla de personalització de xats.
2. Accedir a la carpeta d'imatges de l'ordinador per tal de seleccionar la nova fotografia de fons de pantalla.
3. Un cop seleccionada la fotografia, per determinar-la com a fons de pantalla a la pantalla de Xats de l'usuari.

- Crear Xats (pes 5): Es poden crear xats grupals o individuals: Per crear un xat es realitzaran 3 esdeveniments:
1. Seleccionar l'opció de Crear Xat.
2. Determinar les persones amb les quals es vol crear el Xat, poden ser 1 o moltes i introduir el nom del Xat en cas de ser un Xat grupal.
3. Donar-li a acceptar es crea el Xat informant a tots els participants d'aquest.

- Afegir-se a un Xat (pes 5): Per afegir-se a un Xat es realitzaran 3 esdeveniments:
1. Buscar al cercador de Xats el nom del Xat al qual es vol afegir.
2. Apareixeran la llista dels xats amb el nom igual o semblant.
3. Es clicarà al botó d'afegir-se on entrarà al Xat.

- Gestionar usuaris d'un xat (pes 10): Per gestionar usuaris d'un Xat es realitzaran 4 esdeveniments:
1. Veure una llista dels usuaris que formen part del Xat en qüestió.
2. Seleccionar l'usuari en cas de voler treure un usuari del xat o clicar a l'opció d'afegir participant per fer una cerca en el cas de voler afegir un usuari del Xat.
3. Sortirà un missatge preguntant si està segur de voler treure a l'usuari del Xat o sortirà el missatge preguntat si està segur de voler afegir a l'usuari al Xat.
4. Surt un missatge al Xat, notificant als participants de què l'usuari ja no forma part del Xat o es notificarà als participants del Xat de què hi ha un participant més, indicant el seu nom.

- Sortir d'un Xat (pes 5): Per sortir d'un Xat es realitzaran 3 esdeveniments:
1. Entrar al Xat del qual es vol sortir i clicar al botó SORTIR.
2. Apareixerà un missatge preguntant si està segur de sortir del Xat, Acceptar.
3. Apareixerà un missatge al Xat notificant als participants d'aquest que l'usuari en qüestió ha sortit.

- Crear Xat Predefinit (pes 5): Per crear un Xat Predefinit s'usaran els mateixos esdeveniments que per crear un Xat normal (veure més amunt).

- Gestionar Xat Predefinit (pes 5): Per gestionar un Xat Predefinit s'usaran els mateixos esdeveniments que gestionant un Xat normal (veure més amunt).

- Gestionar Comptes (pes 5): Per gestionar els comptes s'usaran 3 esdeveniments:
1. Seleccionar l'usuari amb el qual es vol treballar
2. Esborrar el compte o fer el necessari.

![Imgur](http://i.imgur.com/Vujx2AQ.png)

![Imgur](http://i.imgur.com/owd7lpD.png)

**TF = (pes*prioritat) = 51.5**

#### TCF = 0.6 + (TF/100) = 1.115

![Imgur](http://i.imgur.com/FRNuLnB.png)

![Imgur](http://i.imgur.com/s2WHrEq.png)

**EF = (pes * avaluació) = 14.5**

#### ECF = 1.4 + (-0.03*EF) = 0.965


## UCP = (UAW+UUCW) * TCF * ECF = 157.09 ##

- PF = 20, Ja que no tenim projectes antics ni experiència, assignem el valor 20, ja que és un valor neutre entre 15 i 30, sortiran uns números bastant redons.

## ESTIMACIÓ DE TEMPS = PF * UCP = 20 * 135.57285 = 3141.85 ##


### 2.2. Estimació de cost ###

![Imgur](http://i.imgur.com/uvyakS9.png)

![Imgur](http://i.imgur.com/AYBYtbG.png)

Per calcular l'esforç total es multiplica cada percentatge d'Effort pel percentatge de cada rol en cada fase.

![Imgur](http://i.imgur.com/9Tfldd9.png)

Per calcular les hores per fase/rol, es multiplica la dedicacio del rol/fase * est. temps * effort de la fase.

![Imgur](http://i.imgur.com/8FWAHoX.png)

Per calcular les hores de fase/persona, es divideix pel numero de persones del carrec.

![Imgur](http://i.imgur.com/oyWhbbB.png)

![Imgur](http://i.imgur.com/05upQfB.png)

- Personal: Nombre de persones que ocuparan cada càrrec.
- Sou (Cost/hora): El sou de cada càrrec ha estat extret de diferents fonts, sempre basant-nos en números certs per alguna empresa real.
- Esforç: Calculat a la taula de Dedicació prevista pels rols.
- Hores/Càrrec: Calculat a la taula d'Hores previstes pels rols.
- Hores/Persona: Calculat a la taula d'Hores previstes per persona.
- Cost Càrrec: Calculat mitjançant la multiplicació d'Hores/Càrrec per Sou.
- Cost Persona: Calculat mitjançant la multiplicació d'Hores/Persona per Sou.
- Seguretat Social (calculat per persona): Calculat mitjançant la multiplicació de Cost Persona * 0.4 (40%)
- Euros Fixes: 200€ fixes en termes de lloc de treball.
- SS + C/Pers + E.fixos: Calculat sumant la SS, el Cost/Persona i els 200€ d'euros fixos.
- Despeses Estructurals (corresponen a un 15%): Calculat mitjançant la multiplicació de SS+C/P+E.fixes * 0.15 ja que les despeses estructurals corresponen a un 15%.
- Total Brut/Persona: Calculat mitjançant la suma de les Despeses Estructurals i SS+C/P+E.fixes.
- Total Brut/Càrrec: Calculat mitjançant la multiplicació del Total Brut/Persona pel Personal.

Amb això ens queda un total de 89.774,30 € on afegirem en 50% de beneficis i el 10% de contingències, el que ens donarà el total final de 143.638,88 €

** BENEFICI (50%) = 44.887,15 € **

** Contingències (10%) = 8.977,43 € **

## TOTAL = 143.638,88 € ##


## 3. PLA DE FASES ##

### A) DISTRIBUCIÓ DE CASOS D'ÚS PER FASES ###

|   										|   INCEPTION   |  ELABORATION  | CONSTRUCTION | TRANSITION |
|-------------------------------------------| :--------- 	| :-------------| :------------| :----------|
| Registrar-se 								|  Identificat  |    Complet    |    Complet   |   Complet  |
| Gestionar Dades Personals 				|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Aceptar Sol·licitud d'amistad 			|  Identificat  |    Complet    |    Complet   |   Complet  |
| Rebutjar Sol·licitud d'amistad 			|  Identificat  |    Complet    |    Complet   |   Complet  |
| Enviar Sol·licitud d'amistad 				|  Identificat  |    Complet    |    Complet   |   Complet  |
| Crear Esdeveniment Obert 					|  Identificat  |    Complet    |    Complet   |   Complet  |
| Crear Esdeveniment Tancat 				|  Identificat  |    Complet    |    Complet   |   Complet  |
| Unir-se a un Esdeveniment 				|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Cancel·lar assistencia a un Esdeveniment 	|  Identificat  |    Esbossat   |    Refinat   |   Complet  |
| Compartir Imatges 					  	|  Identificat  |    Esbossat   |    Refinat   |   Complet  |
| Personalitzar Xat 						|  Identificat  |    Esbossat   |    Refinat   |   Complet  |
| Crear Xat 								|  Identificat  |    Complet    |    Complet   |   Complet  |
| Crear Xat Predefinit 						|  Identificat  |    Complet    |    Complet   |   Complet  |
| Afegir-se a un Xat 						|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Gestionar Usuaris d'un Xat 				|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Gestionar Xat Predefinit					|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Sortir d'un Xat 							|  Identificat  |    Refinat    |    Complet   |   Complet  |
| Gestionar Comptes 						|  Identificat  |    Esbossat   |    Refinat   |   Complet  |


![Imgur](http://i.imgur.com/h1HqS1y.png)

![Imgur](http://i.imgur.com/d6z6Wxa.png)

### B) INFORMACIÓ DE FASES ###

**INCEPTION**

Iteració 1, I1:

*Objectius:*

- Definir la visió del producte
- Determinar l'abast del projecte (Nombre d'usuaris finals aproximat)
- Crear el cas de negoci
- Detallar els requisits
- Determinar els casos d'ús
- Definir l'arquitectura idònia per al sistema
- Crear el pla de desenvolupament de software

**ELABORATION**

Iteració 1, E1

*Objectius:*

- Instal·lació i proves de l'arquitectura
- Validació dels detalls dels requisits
- Implementar els casos d'ús principals

Iteració 2, E2

*Objectius:*

- Reduir els possibles riscos de l'arquitectura
- Detallar i refinar els casos d'ús dependents directament dels principals implementats

**CONSTRUCTION**

Iteració 1, C1

*Objectius:*

- Refinar tots els casos d'ús restants
- Validació dels casos d'ús implementats

Iteració 2, C2

*Objectius:*

- Implementar els casos d'ús
- Integrar el producte i validar l'estat

Iteració 3, C3

*Objectius:*

- Validació dels casos d'ús implementats
- Planificar la versió beta i el suport a l'usuari

**TRANSITION**

Iteració 1, T1:

*Objectius:*

- Desplegar la beta en els clients
- Obtenir i processar feedback
- Finalitzar el suport a l'usuari
- Sortida al mercat

![Imgur](http://i.imgur.com/hR00rq1.png)
