# SISTEMA SocMus - ESPECIFICACIÓ DE REQUISITS DEL SOFTWARE #

## 1. ESPECIFICACIÓ FUNCIONAL ##

### 1.1. Diagrama de casos d'ús

![Casos d'us](http://i.imgur.com/nWzSIN3.png)

- Cas d'ús UC001 - Registrar-se: Es crea un nou usuari amb les dades que la persona introdueixi.

- Cas d'ús UC002 - Gestionar Dades: L'usuari pot gestionar les dades que havia introduït, incloent-hi el seu correu, nom i contrasenya entre d'altres.

- Cas d'ús UC003 - Gestionar Sol·licituds d'amistat: L'usuari pot acceptar, rebutjar o enviar sol·licituds d'amistat a altres usuaris de l'aplicació.

- Cas d'ús UC004 - Crear Esdeveniment: L'usuari crea un esdeveniment, ja sigui obert (per a tothom) o tancat (per invitació).

- Cas d'ús UC005 - Cancel·lar assistència a un esdeveniment: Permet a l'usuari cancel·lar la seva assistència a un esdeveniment.

- Cas d'ús UC006 - Afegir-se a un esdeveniment: L'usuari passa a formar part de l'esdeveniment en qüestió, si es tracta d'un esdeveniment tancat, l'usuari ha d'haver estat prèviament convidat.

- Cas d'ús UC007 - Compartir imatges: L'usuari compartirà imatges amb els altres participants de l'esdeveniment, per així fer-les més accessibles a tots els membres de l'esdeveniment.

- Cas d'ús UC008 - Personalitzar Xat: L'usuari podrà personalitzar els seus xats, tenint l'opció de canviar la imatge de fons entre altres coses.

- Cas d'ús UC009 - Crear Xat: L'usuari crearà un xat i en passarà a ser l'administrador, ja sigui individual (amb un altre usuari), grupal obert (per a qualsevol usuari que vulgui unir-s'hi) o grupal tancat (pels usuaris als quals l'administrador vulgui afegir).

- Cas d'ús UC010 - Gestionar usuaris d'un xat: Un cop l'usuari ha creat un xat grupal, serà capaç de gestionar els participants que hi haurà, afegint-ne de nous o eliminant-ne dels ja existents.

- Cas d'ús UC011 - Afegir-se a un xat: L'usuari podrà afegir-se a un xat grupal obert creat per un altre usuari.

- Cas d'ús UC012 - Sortir d'un xat: L'usuari podrà sortir d'un xat dels que formava part.

- Cas d'ús UC013 - Crear xat predefinit: L'usuari administrador podrà crear un xat predefinit accessible per a tots els usuaris.

- Cas d'ús UC014 - Gestionar xat predefinit: L'usuari administrador podrà gestionar els usuaris d'un xat predefinit i expulsar-ne algun si ho veu necessari.

- Cas d'ús UC015 - Gestionar comptes: L'usuari administrador podrà donar de baixa, comptes conflictius o que ell cregui necessari.


### 1.2. Descripció individual dels casos d'ús

#### Cas d'ús UC001 - Registrar-se ####

L'usuari accedeix per primer cop a l'aplicació, i mitjançant camps de text es crea una compta a l'aplicació, el sistema registra aquesta creació i crea el compte. L'usuari haurà d'especificar el seu nom i els seus cognoms, així com la adreça de correu electrònic, les llengües que parla o que està interessat a parlar i els interessos que té per tal de passar a formar part de grups amb les mateixes preferències.

#### Cas d'ús UC002 - Gestionar Dades ####

L'usuari accedeix al seu perfil personal i des d'allà té l'opció de gestionar les seves dades personals, és a dir, modificar els camps amb els quals es va registrar inicialment, un cop realitzats els canvis i fer click al botó d'acceptar, el sistema enregistrarà aquests canvis i modificarà la informació guardada sobre l'usuari que s'està tractant. A més a més, podrà modificar la seva foto de perfil i gestionar camps menys importants i no accessibles al moment de registrar-se com pot ser afegir un "alies".

#### Cas d'ús UC003 - Gestionar Sol·licituds d'amistat ####

L'usuari accedeix al submenú de sol·licituds d'amistat i té l'opció de gestionar-les:

- Acceptar: L'usuari accepta la sol·licitud d'amistat i el sistema enregistra aquesta sol·licitud, a la vega el sistema envia una notificació a l'usuari que va enviar la sol·licitud inicialment per a saber que ha estat confirmada.

- Rebutjar: L'usuari rebutja la sol·licitud d'amistat i el sistema enregistra que la sol·licitud ha estat rebutjada.

- Enviar: L'usuari selecciona un altre usuari al qual enviar una sol·licitud d'amistat, el sistema envia aquesta sol·licitud juntament amb una notificació a l'usuari destí per a què aquest pugui acceptar-la o rebutjar-la.


#### Cas d'ús UC004 - Crear Esdeveniment ####

L'usuari passa a crear un esdeveniment, mentre l'usuari crea aquest esdeveniment, haurà de seleccionar diverses coses, com per exemple on es produirà l'esdeveniment o quan es produirà l'esdeveniment, també podrà invitar a altres usuaris o esperar al fet que s'hi uneixin els qui ho vulguin, a més a més l'usuari podrà afegir comentaris sobre l'esdeveniment com a consells per als quals s'hi afegeixin o establir un nombre màxim de participants, un cop l'usuari ha creat l'esdeveniment, el sistema enregistra les dades introduïdes i el crea a la base de dades de l'aplicació.

#### Cas d'ús UC005 - Cancel·lar assistència a un esdeveniment ####

L'usuari accedirà als esdeveniments que està inscrit i podrà cancel·lar la seva assistència a algun d'aquests esdeveniments, quan l'usuari cancel·li l'assistència el sistema li enviarà un missatge de confirmació, si es confirma aquest missatge, el sistema cancel·larà l'usuari de l'esdeveniment i enviarà una notificació al creador de l'esdeveniment sobre l'absència del participant en l'esdeveniment.

#### Cas d'ús UC006 - Afegir-se a un esdeveniment ####

L'usuari escollirà un esdeveniment de la llista d'esdeveniments oberts disponibles i s'hi afegirà, el sistema enviarà una notificació a l'administrador de l'esdeveniment per a notificar-lo de què tindrà un nou assistent, si es tractava d'un esdeveniment tancat, l'usuari s'afegirà a l'esdeveniment acceptant la sol·licitud que haurà rebut del creador de l'esdeveniment.

#### Cas d'ús UC007 - Compartir imatges ####

L'usuari d'un esdeveniment podrà compartir imatges de l'esdeveniment amb tots els membres de l'esdeveniment mitjançant un servei extern de Google Drive, un cop compartides les imatges el sistema enviarà una notificació als altres assistents perquè puguin accedir a les imatges, aquestes imatges només estaran visibles per als usuaris d'aquest esdeveniment.

#### Cas d'ús UC008 - Personalitzar Xat ####

L'usuari accedirà a la configuració del xat i des d'allà podrà canviar el nom del xat la imatge de fons, el sistema permetrà a l'usuari escollir una imatge del dispositiu o bé fer-ne una de nova, un cop acceptat el sistema canviarà la informació del xat per la nova informació actualitzada.

#### Cas d'ús UC009 - Crear Xat ####

L'usuari clicarà a l'opció de crear un nou xat del qual en serà l'administrador, el sistema li donarà a escollir a l'usuari si el xat serà individual (amb un altre usuari), grupal obert (per a qualsevol usuari que vulgui unir-s'hi) o grupal tancat (pels usuaris als quals l'administrador vulgui afegir), un cop escollir l'usuari haurà d'afegir els usuaris que vulgui, haurà de triar un nom pel grup i podrà seleccionar una imatge de fons que el sistema enregistrarà.

#### Cas d'ús UC010 - Gestionar usuaris d'un xat ####

Després d'haver creat un xap grupal, l'usuari (que serà l'administrador del xat) podrà gestionar els participants que hi haurà, afegint-ne de nous o eliminant-ne els ja existents. En els dos casos el sistema enviarà notificacions als usuaris afectats notificant-los de l'actualització del xat, per afegir-lo o per eliminar-lo del xat.

#### Cas d'ús UC011 - Afegir-se a un xat ####

L'usuari podrà escollir qualsevol xat grupal de la llista de xats grupals oberts i afegir-s'hi, un cop seleccionat el xat el sistema enviarà una confirmació a l'usuari administrador del xat.

#### Cas d'ús UC012 - Sortir d'un xat ####

L'usuari accedirà a qualsevol dels xats dels quals forma part i sortirà d'aquest xat, el sistema enviarà un missatge de confirmació abans de sortir definitivament del xat, i en cas de confirmar-lo el sistema traurà a l'usuari del xat.

#### Cas d'ús UC013 - Crear xat predefinit ####

L'usuari administrador podrà crear un xat predefinit accessible a tots els usuaris, el sistema deixarà triar un nom pel grup i permetrà afegir una imatge de fons per al xat.

#### Cas d'ús UC014 - Gestionar xat predefinit ####

L'usuari administrador podrà gestionar els xats predefinits: canviar el nom, canviar la foto de portada i fer fora un usuari si ho creu necessari. El sistema serà l'encarregat de gestionar aquests canvis i de notificar als usuaris implicats en alguna acció si és necessari.

#### Cas d'ús UC015 - Gestionar comptes ####

L'usuari administrador rebrà comentaris o queixes d'usuaris i podrà donar de baixa, comptes conflictius si així ho creu necessari, en cas de donar de baixa una compta, el sistema, serà l'encarregat d'eliminar aquest compte i d'eliminar tot el que hagués fet anteriorment, així com eliminar-lo dels xats i esdeveniments als quals estava inscrit i eliminar a l'usuari de la llista d'amistats dels altres usuaris enviant-los prèviament una notificació.


## 2. ESPECIFICACIÓ NO FUNCIONAL ##

#### Requisit NFR001 - *Estabilitat* ####
En cap cas l'usuari pot realitzar una acció que produeixi errors en el sistema per motius de fiabilitat en l'aplicació.

*Condició de satisfacció:* Abans de qualsevol versió el sistema haurà de passar tests de qualitat que provin totes les funcionalitats disponibles per als usuaris de SocMus.

#### Requisit NFR002 - *Concurrència* ####
La web així com el servidor i la base de dades han de poder respondre de manera correcta a possibles peticions simultànies que diferents usuaris actius puguin fer en un moment concret.

*Condició de satisfacció:* S'aplicarà un test d'estrès de manera periòdica en els moments de més baixa activitat per a comprovar la seva resposta. D'altra banda el nombre de peticions fetes als tests dependrà dels usuaris que l'aplicació tingui proporcionalment.

#### Requisit NFR003 - *Mantenibilitat* ####
- La base de dades ha de tenir una estructura que permeti escalar el sistema de forma àgil, ràpida i coherent.
- Per a la REST API del servidor s'ha de fer un control de versions amb l'objectiu de mantenir totes les funcionalitats del sistema actives sense que els usuaris finals vegin afectats els seus hàbits en la xarxa.

*Condició de satisfacció:* La base de dades ha d'estar ben dissenyada. El control de versions ha de permetre diferenciar entre versions que amplien funcionalitats del sistema i versions que trenquin antigues funcionalitats i, amb conseqüència, la seva actualització a la web ha de ser immediata.

#### Requisit NFR004 - *Interfície* ####
Cal dissenyar una interfície intuïtiva i fàcil d'utilitzar per a tot usuari de SocMus, només així mantindran interès en la xarxa i seran usuaris actius d'aquesta.

*Condició de satisfacció:* Tot disseny que afecti la interfície de l'usuari, haurà de passar tests de UX i UI.

#### Requisit NFR005 - *Seguretat* ####
Tota persona que utilitzi el sistema espera que xats, imatges o informació personal entre d'altres sigui totalment privada, sempre que no la vulgui fer pública.

*Condició de satisfacció:* Les comunicacions seran per https a més d'anar encriptades totes les dades. Passaran periòdicament tests de seguretat per tal d'assegurar que les dades no són vulnerables.

#### Requisit NFR006 - *Escalabilitat* ####
La pàgina web ha de tenir la capacitat d'augmentar el nombre de servidors per poder atendre un increment del nombre d'usuaris.

*Condició de satisfacció:* La pàgina web ha d'estar programada per tal de poder rebre informació de nous servidors. S'aplicarà un test periòdicament que consistirà a incrementar de forma sobtada el nombre de registres de nous usuaris.

#### Requisit NFR007 - *Disponibilitat* ####
Qualsevol usuari ha de poder entrar a la pàgina web i poder realitzar qualsevol operació sense que aquesta es pengi. No es pot donar el cas que un usuari no pugui accedir al sistema.

*Condició de satisfacció:* S'aplicarà un test en què molts usuaris accedeixin a la vegada a la pàgina per comprovar que no n'hi hagi cap que no hi pugui accedir.

#### Requisit NFR008 - *Usabilitat* ####
Facilitat que tenen els usuaris d'utilitzar la pàgina web. Molt lligada al disseny i la comunicació d'interfícies gràfiques. Permet tres millores:
- Més eficiència, es pot acabar una tasca concreta en menys temps.
- Més inductivitat o facilitat d'aprenentatge, el funcionament de la pàgina es pot deduir observant-la.
- Més satisfacció de l'usuari.

*Condició de satisfacció:* Realitzar una prova per avaluar la usabilitat amb usuaris reals en un context d'ús el més real possible.

#### Requisit NFR009 - *Cost* ####
Minimitzar els costos econòmics i temporals (en nombre d'hores dedicades) que pugui tenir la pàgina.

*Condició de satisfacció:* Realitzar un pla de negoci abans de començar a crear la pàgina i revisar-lo periòdicament per no accedir-nos amb els recursos i que tot estigui correcte.

#### Requisit NFR010 - *Operativitat* ####
Que la pàgina web és operativa, és a dir, que funciona correctament.

*Condició de satisfacció:* Realitzar una prova per comprovar que totes les funcionalitats de la pàgina funcionen correctament.

## 3. MOCK-UPS ##

### PANTALLA D'INICI DE SESSIÓ

![LOGIN](http://i.imgur.com/c8Wk3Pd.jpg)
![LOGIN MOVIL](http://i.imgur.com/fvjUDYo.png)


### PANTALLA D'ESDEVENIMENTS

![ESDEVENIMENTS](http://i.imgur.com/B0LKXzS.png)
![ESDEVENIMENTS MOVIL](http://i.imgur.com/rzaulZt.png)

### PANTALLA DE XATS

![XATS](http://i.imgur.com/Wy3G6sL.png)
![XATS MOVILS](http://i.imgur.com/wN45F86.png)