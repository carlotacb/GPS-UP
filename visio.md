# SISTEMA SocMus - VISIÓ #

## 1. INTRODUCCIÓ ##

Universitats de tot el món tenen acords i convenis amb universitats o institucions de diferents països. Tots aquests acords permeten als estudiants realitzar una estada a una universitat estrangera i aprendre conceptes nous a la vegada que practiquen l'idioma on estan però tot i els avantatges que els programes ofereixen, és amb la vida quotidiana on s'intercanvien experiències entre estudiants i és en aquest àmbit on neix SocMus, una nova xarxa social per apropar tot estudiant a la vida universitària.

Indicant algunes dades bàsiques com els teus interessos així com els idiomes que saps parlar o vols aprendre l'aplicació serà capaç de proposar-te esdeveniments creats per altres usuaris a prop teu que t'interessin.

D'altra banda SocMus més enllà de ser una xarxa focalitzada als estudiants internacionals, tindrà xats predeterminats oberts per idiomes per tota persona que els vulgui practicar i la capacitat de crear xats individuals per comunicar-te de forma directa amb altres usuaris.

Per a tots els comerços de la ciutat i més concretament de l'entorn universitari SocMus suposa una gran oportunitat per promoure's així com donar a conèixer els seus productes i/o serveis.

## 2. EL PROBLEMA ##

Els programes d'intercanvi europeus entre estudiants universitaris estan fortament estesos però el seu àmbit d'actuació queda restringit en quasi tots els casos en l'educatiu.
D'altra banda totes les persones que van estudiar a l'estranger no troben referències personalitzades de coses a fer o directament llocs que visitar més enllà de guies turístiques, enfocades per altres tipus d'usuaris (turisme vacacional o puntual).

Així doncs SocMus pretén ser una xarxa social que fa èmfasi amb un objectiu més social i cultural per als estudiants, fomentant les relacions entre els individus així com amb el comerç de la ciutat i voltants, basant-se en els interessos de cada usuari.

## 3. PARTS INTERESSADES ##

1. *Estudiants*
Els usuaris troben l'oportunitat d'aprendre idiomes sense necessitat d'apuntar-se a plataformes alienes a la vida universitària, a la vegada que es fomenta la cohesió de la comunitat educativa.
2. *Comerços o serveis*
Tots els comerços i/o serveis de la ciutat o de la zona veuen oberta una nova via de publicitat a la vegada que poden promocionar els seus productes i/o serveis disponibles.
*Responsabilitats:* Oferir descomptes en els seus productes i/o serveis amb l'objectiu de promocionar l'aplicació entre els universitaris i universitàries.
3. *Universitats*
Promovent l'aplicació guanyen reconeixement en l'àmbit social, poden destacar la seva millora per als estudiants internacionals i aprofitar aquesta eina per arribar a acords amb altres entitats o institucions donada la seva capacitat de promoció.
*Responsabilitats:* Són l'essència de la xarxa, qui la fa possible. Només amb la seva promoció interna pot arribar als i les estudiants.

## 4. EL PRODUCTE ##

La pàgina serà una xarxa social que permetrà posar en contacte estudiants de la mateixa universitat amb estudiants d'Erasmus. Cada estudiant tindrà un perfil propi i podrà fer-se amic dels perfils dels altres estudiants. Hi ha xats predeterminats. L'estudiant podrà establir xats individuals i grupals amb els altres estudiants. L'estudiant podrà crear esdeveniments.

### 4.1. Perspectiva del producte ###

Crear una xarxa social amb un servidor amb la tecnologia [Node JS][2] i [Express][3] per a tenir una REST API amb l'objectiu de reutilitzar crides i funcionalitats del servidor entre web i aplicacions mòbils.

![Imgur](http://i.imgur.com/oGHC7iN.png)

### 4.2. Descripció del producte ###

1. *Enviar sol·licitud d'amistat*. L'estudiant podrà enviar una sol·licitud d'amistat als altres estudiants a través dels seus perfils
2. *Acceptar sol·licitud d'amistat*. L'estudiant podrà acceptar una sol·licitud d'amistat enviada per un altre estudiant.
3. *Rebutjar sol·licitud d'amistat*. L'estudiant podrà rebutjar una sol·licitud d'amistat enviada per un altre estudiant.
4. *Crear xat individual*. L'estudiant podrà crear un xat individual amb un altre estudiant.
5. *Crear xat grupal tancat*. L'estudiant podrà crear un xat grupal amb els estudiants que seleccioni.
6. *Crear xat grupal obert*. L'estudiant podrà crear un xat grupal obert.
7. *Afegir-se a un xat grupal obert*. L'estudiant podrà afegir-se a un xat grupal obert.
8. *Crear esdeveniment tancat*. L'estudiant podrà crear un esdeveniment amb els estudiants que seleccioni.
9. *Crear esdeveniment obert*. L'estudiant podrà crear un esdeveniment obert.
10. *Afegir-se a un esdeveniment obert*. L'estudiant podrà afegir-se a un esdeveniment obert.

### 4.3. Supòsits de funcionament ###

1. *Descomptes*. Els comerços i serveis de la ciutat accedeixen a oferir descomptes als membres de la xarxa.
2. *Promoció*. Les universitats així com els usuaris i els comerços promocionen la seva utilització.
3. *Interès*. El producte produeix l'interès desitjat en els seus usuaris.

### 4.4. Dependències sobre altres sistemes ###

1. *Servidor extern*. És el centre de SocMus, ha de poder respondre a totes les peticions que li puguin fer i no col·lapsar-se.   
2. *Base de dades externa*. Ha de fer backups periòdicament així com tenir les dades dels usuaris protegides. D'altra banda no ha d'estar limitada per espai.

### 4.5. Altres requisits ###

1. *Estabilitat*
En cap cas l'usuari pot realitzar una acció que produeixi errors en el sistema per motius de fiabilitat en l'aplicació.

2. *Concurrència*
La web així com el servidor i la base de dades han de poder respondre de manera correcta a possibles peticions simultànies que diferents usuaris actius puguin fer en un moment concret.

3. *Mantenibilitat*
La base de dades ha de tenir una estructura que permeti escalar el sistema de forma àgil, ràpida i coherent. Per a la REST API del servidor s'ha de fer un control de versions amb l'objectiu de mantenir totes les funcionalitats del sistema actives sense que els usuaris finals vegin afectats els seus hàbits en la xarxa.

4. *Interfície*
Cal dissenyar una interfície intuïtiva i fàcil d'utilitzar per a tot usuari de SocMus, només així mantindran interès en la xarxa i seran usuaris actius d'aquesta.

5. *Seguretat*
Tota persona que utilitzi el sistema espera que xats, imatges o informació personal entre d'altres sigui totalment privada, sempre que no la vulgui fer pública.

6. *Escalabilitat*
La pàgina web ha de tenir la capacitat d'augmentar el nombre de servidors per poder atendre un increment del nombre d'usuaris.

7. *Disponibilitat*
Qualsevol usuari ha de poder entrar a la pàgina web i poder realitzar qualsevol operació sense que aquesta es pengi. No es pot donar el cas que un usuari no pugui accedir al sistema.

8. *Usabilitat*
Facilitat que tenen els usuaris d'utilitzar la pàgina web. Molt lligada al disseny i la comunicació d'interfícies gràfiques. Permet tres millores:
- Més eficiència, es pot acabar una tasca concreta en menys temps.
- Més intuïtivitat o facilitat d'aprenentatge, el funcionament de la pàgina es pot deduir observant-la.
- Més satisfacció de l'usuari.

9. *Cost*
Minimitzar els costos econòmics y temporals (en nombre d'hores dedicades) que pugui tenir la pàgina.

10. *Operativitat*
Que la pàgina web és operativa, és a dir, que funciona correctament.


## 5. RECURSOS ##

[1] http://www.fib.upc.edu/fib/erasmus.html

[2] https://nodejs.org/

[3] http://expressjs.com/
