
# COMANDAMENTS

EXECUTAR JS A LA TERMINAL:
<div class="exemple">

```cs
Obrim terminal -> ens posem dins la carpeta de l'arxiu -> node arixu.js
```
</div>

<br>
EXCRIURE EN DIVERSES LINIES ALHORA
<div class="exemple">

```cs
option+command
seleccionem les linies amb les fletches
escrivim el que vulguem
per sortir de la selecció apretem ESC
```
</div>



<br><br><br><br><br><br><br>

<style>
    .defi{
        background-color: rgb(255,255,100);
    }
    .tradu{
        background-color: rgb(0,150,100);
    }
    .exemple{
        
        background-color: #b3ecff;
    }
</style>

Per veure el codi que emet el script en un fitxer HTML, podem obrir el navegador i usar ```Command + Option + J````

<div class="defi">

```cs
<script>
    console.log("Hola");
</script>
```
</div>

![Getting Started](./ImatgesJS/Consola.png)


# Creem un fixer JS
Extensió: .js

<div class="defi">

```cs
console.log("Print === console.log("");");
```
</div>

# Comentaris
<div class="exemple">

```cs
// Comentari

/* Comentari
diverses
línies*/
```
</div>






# Variables
- Undefined
La variable encata no té un valor assignat; se li assigna per defecte.
- Null
- Boolean
- String
- Symbol
- Number 
- Object


S'utilitza CAMELCASE: si tenim més d'una paraula, comencem amb minúscula i la següent enganxada amb Majúscula.
laMevaVariable.



## Consideracions

-SENSIBLE A MAJÚSCULES I MINÚSCULES.

-Existeix INFINITY.

-Utilitzem '.' pels decimals.

# Cadenes de caràcters
" " == ' '

- Cadenes amb cometes simples:
Podem escapar de les cometes dobles dins d'una cadena utilitzant \ abans.

<div class="exemple">

```cs
var unaFrase = "Aprendre a programar amb \"JS\"";
```
</div>

O bé utilitzant cometes simples
<div class="exemple">

```cs
var unaFrase = 'Aprendre a programar amb "JS"';
```
</div>


Podem juntar STRINGS utilitzant ```"Alan"+"Gold"```.
També podem ajuntar STRINGS i variables:

<div class="exemple">

```cs
var num=10;
var missatge = "Tinc " + num + " llibres."
console.log(missatge);
```
</div>

## Immutabilitat de les cadenes

No podem modificar elements de cadenes, però podem canviar la cadena sencera.

# Seqüències d'escapament:
- \'    Cometes simples
- \"    Cometes dobles
- \\    Barra invertida
- \n    Línia nova
- \r    Retorn de Carro
- \t    Tabulador
- \b    Retrocés
- \f    Salt de pàgina



# Operacions comunes

- variable.length
- Índex de posició: variable[i]


# Llistes
<div class="exemple">

```cs
var notes = ['John', 95, 67];
```
</div>
var notes = ['John', 95, 67];



# Arreglos / arrays
<div class="exemple">

```cs
var arreglo = [10, 20, 30];
var suma = arreglo[0] + arreglo[1] + arreglo[2];
console.log(suma);
arreglo[1] = [4,5,6];
arreglo[2] = "Exemple"
console.log(arreglo);
```
</div>

# .PUSH(), .POP(), .SHIFT(), .UNSHIFT()
- PUSH: Agregar elements a una cadena.
<div class="exemple">

```cs
var estacions = ["Hivern", "Estiu", "Primavera"];
estacions.push("Tardor");
console.log(estacions)
```
</div>

Obtenim:
<div class="defi">

```cs
['Hivern', 'Estiu', 'Primavera', 'Tardor']
```
</div>

- POP: Elimina l'últim element de la cadena:
<div class="exemple">

```cs
eliminacio = estacions.pop();
console.log(estacions);
```
</div>

Obtenim:
<div class="defi">

```cs
 ['Hivern', 'Estiu', 'Primavera']
```
</div>

- .SHIFT: Elimina el primer element de la cadena:

<div class="exemple">

```cs
shiftPrimer = estacions.shift();
console.log(estacions);
```
</div>

Obtenim:
<div class="defi">

```cs
 ['Estiu', 'Primavera']
```
</div>

- .UNSHIFT() : Agregar elements davant d'un arreglo.



# Funcions

<div class="tradu">

```cs
function nomFuncio(){
    console.log("La funció printa");
}

nomFuncio();
```
</div>

# Variables Globals i Locals
Les varibales globals les podem utilitzar en tot el programa, però les variables locals només les podem utilitzar a les funcions on estan definides.

- Si tenim una v.global i una v.local amb el mateix nom, el programa executarà la local només si cridem la seva funció.

<div class="exemple">

```cs
meuNom = "Sandra"
function nom (){
    var meuNom = "Natàlia";
    console.log(meuNom);
}
nom();
console.log(meuNom);

```
</div>
Obtenim:
<div class="exemple">

```cs
Natàlia
Sandra

```
</div>


# JSON
Podem printar algunes cadenes de manera més maca:
<div class="exemple">

```cs
console.log("Abans: " + vectorExemple);
console.log("Abans: " + JSON.stringify(vectorExemple));
```
</div>

<div class="defi">

```cs
Abans: 1,2,3,4
Abans: [1,2,3,4]
```
</div>


# Comparador de dades
<div class="exemple">

```cs
console.log(9 == 9)   //Return true
console.log(9 == "9")   //Return true
```
</div>

Si enlloc de comparar el contingut de les dades volem comparar el tipus, utilitzem === :

<div class="defi">

```cs
console.log(9 === "9")   //Return false
```
</div>

- Observació: passa el mateix amb '''!=''' i '''!=='''

- Podem comparar lletres per ordre alfabètic
<div class="defi">

```cs
console.log("B" > "M")   //Return false
console.log("Martell" > "Hola")   //Return true (M > H)
```
</div>


# Objectes
Ens permeten guardar la seqüència d'un conjunt de propietats relacionades amb els seus corresponents valors.

<div class="exemple">

```cs
// meuGos és l'objecte
var meuGos = {
    "nom" : "Chia",
    "edat" : 5,
    "pes" : 11,
    "raça" : "podenca",
    "pais de residencia" : "Barcelona"
};
```
</div>

- Curiositat : Podem expressar propietats amb números:

<div class="exemple">

```cs
// meuGos és l'objecte
var meuObjecte{
    5 : "cinc"
};
```
</div>

Per accedir a les propietats escrivim el nom de la variable.propietat:
<div class="exemple">

```cs
console.log(meuGos.nom)
```
</div>

Si volem accedir a alguna propietat que té més d'una paraula (i, per tant, espais), utilitzem la notació de corchets:

<div class="exemple">

```cs
console.log(meuGos["pais de residencia"]);

// ---> Barcelona
```
</div>


Per accedir-hi utilitzant variables:
<div class="exemple">

```cs
var resultats = {
    1 : "bgui111",
    2 : "hiudf222",
    3 : "miof333",
    4 : "cnjd444"
};

var posicio = 2;
console.log(resultats[posicio]);
```
</div>

Per modificar el valor d'un objecte, simplement el cridem i li assignem el nou:
<div class="exemple">

```cs
resultats[2] = "slpi555";
console.log(resultats[2]);
```
</div>

També podem agregar-li valors:
<div class="exemple">

```cs
var meuGos = {
    nom: ['Chia','Lua'],
    edat: 5,
    pes: 11,
    'raça': 'podenca',
    'pais de residencia': 'Barcelona'
  };


meuGos.nom.push("Durum");
console.log(meuGos);
```
</div>

## Agregar noves propietats:
<div class="defi">

```cs
var meuGos = {
    "raça": "podenca",
    "pais de residencia": "Barcelona"
  };

meuGos["pais d'origen"] = "Granada";
console.log(meuGos);
```
</div>

## Eliminar propietats
<div class="exemple">

```cs
var meuGos = {
    "raça": "podenca",
    "pais de residencia": "Barcelona"
  };

delete meuGos.raça;
console.log(meuGos.raça);

//---> undefined
```
</div>

## Exemple d'associar una propietat amb el seu valor

<div class="exemple">

```cs
function buscarElementQuimic(simbol){
    var elementQuimic = "";

    switch(simbol){
        case "Al":
            elementQuimic = "Alumini";
            break;
        case "Si":
            elementQuimic = "Silici";
            break;
        case "Cl":
            elementQuimic = "Clor";
            break;
        case "He":
            elementQuimic = "Heli";
            break;
        case "Li":
            elementQuimic = "Liti";
            break;
    }
    return elementQuimic;
}
```
</div>

És el mateix que fer

<div class="defi">

```cs
function buscarElementQuimic(simbol){
    var simbolsQuimic={
        "Al" : "Alumini",
        "S" : "Silici",
        "Cl" : "Clor",
        "He" : "Heli",
        "Li" : "Liti"
    };
    return simbolsQuimic[simbol];
}

console.log(buscarElementQuimic("Li"));
```
</div>


## Verificar si existeix una propietat
- .hasOwnProperty()
<br>
<br>
<div class="defi">

```cs
var quadern = {
    "color" : "Verd",
    "categoria" : 3,
    "preu" : 4.56
};

console.log(quadern.hasOwnProperty("color"));

//--->True
```
</div>

Accedir a una variable separada per espais

<div class="defi">

```cs
var quadern = {
    "color" : "Verd",
    "categoria" : 3,
    "preu" : 4.56,
    "numero de pagines": 234
};

console.log(quadern["numero de pagines"]);
console.log(quadern.preu);

//--->234
//--->4.56
```
</div>

Podem crear una funcio que ens ho escrigui:

<div class="exemple">

```cs
var quadern = {
    "color" : "Verd",
    "categoria" : 3,
    "preu" : 4.56
};

console.log(quadern.hasOwnProperty("color"));



function verificarPropietat (objecte, prop){
    if (objecte.hasOwnProperty(prop)==true){
        console.log("Sí té la propietat.");
        console.log("Propietat: "+ objecte[prop]);
        return true;
    } else {
        console.log("No té la propietat");
        return false;
    }
}

verificarPropietat(quadern, "origen");
```
</div>

## Accedir a propietats per variables
<div class="defi">

```cs
var resultat = {
    1: "nora123",
    2: "gina345",
    3: "sol456",
    4: "ros543"
}

var posicio = 2;
console.log(resultat[posicio])


//--->gina345
```
</div>


## Actualitzar, agregar i eliminar propietats a un objecte
<div class="defi">

```cs
var curs = {
    "titol": "Apren JS des de zero",
    "idioma": "Català",
    "duracio": 30
}


curs.visites = 23000
console.log(curs.visites)

curs.duracio = 45
console.log(curs.duracio)


delete curs.idioma;
console.log(curs)

//--->23000
//--->45
//--->{ titol: 'Apren JS des de zero', duracio: 45, visites: 23000 } 
```
</div>

# Objectes complexos
Exemple d'un objecte amb un vector de amb diferents propietats:

L'estructura principal és un "arreglo" (arranjament) on tenim dos objectes (margarita i quatre formatges) separats per comes.

<div class="exemple">

```cs
var comandesPizzes = [
    {
        "tipus": "margarita",
        "mida": "individual",
        "preu": 5.67,
        "toppings": [
            "extra formatge",
            "champinyons",
            "pinya"
        ],
        "perEndur": true
    },
    {
        "tipus": "quatre formatges",
        "mida": "familiar",
        "preu": 18.34,
        "toppings": ["extra formatge", "picant"],
        "perEndur": false
    }
];

console.log(comandesPizzes[0].tipus)
console.log(comandesPizzes[1].toppings[1])


//--->margarita ​​​​
//--->picant
```
</div>

<br>
<br>
<br>
<br>

# Arreglos anidados (arranjaments niats)
Arreglos dentro de arreglos.


<div class="exemple">

```cs
var recepta = {
    "descripcio": "el meu postre preferit",
    "cost": 15.6,
    "ingredients": {
        "massa": {
            "farina": "100 gr",
            "sal": "1 culleradeta",
            "aigua": "1 taça"
        },
        "cobertura":{
            "sucre": "120 gr",
            "chocolata": "4 cullerades",
            "mantega": "200 gr"
        }
    }
}
console.log(recepta.ingredients.massa.aigua);
//--->1 taça
```
</div>

Si vulguéssim seleccionar una propietat segons una variable, o estés separada per espais, la posaríem en corchetes [ ].
<div class="defi">

```cs
console.log(recepta.ingredients["cobertura"].mantega);
//--->200  gr
```
</div>

<br><br><br>

Accedir a un element d'un arreglo anidado.
<div class="exemple">

```cs
var mevesPlantes = [
    {
        tipus: "flors",
        llista: ["roses", "tulipans", "dientes de leon"],
    },
    {
        tipus: "arbres",
        llista: [
            "abet",
            "pi",
            "roure"
        ]
    }
]

var selectorPlanta = mevesPlantes[1].llista[2];
console.log(selectorPlanta);

//--->roure
```
</div>




<br>
<br>
<br>
<br>

# Exemple d'Arr.Anid : COL·LECCIÓ DE DISCOS
## Nova notació

podem prendre una variable i adjudicar-li un valor o, si aquest és UNDEFINED, un altre:
<div class="defi">

```cs
preu = preu || 5;
```
</div>

<div class="exemple">

```cs
/* 
Tenim un objecte que presenta part d'una col·lecicó d'àlbums musicals.

Cada àlbum té un nombre d'identificació únic(id) associat a altres propietats.

No tots els àlbums tenen la informació completa.
*/

var coleccioDiscs = {
    7853: {
        titolAlbum: "Bee Gees Greatest",
        artista: "Bee Gees",
        cançons: ["Stayin Alive"]
    },
    5439:{
        titolAlbum: "ABBA Gold"
    }
}

/* 
Defineix una funció ACTUALITZARDSICS que prengui els paràmetres
discs(objecte que representa la col·lecció de discs), id, propietat(artista o cançons), valor

Completa la funció implementant les següents regles:
    -Si "valor" és una cadena buida, elimina la propietat de l'àlbum corresponent.
    -Si "propietat" és igual que la cadena "cançons"
        -si l'àlbum no té una propietat anomenada "cançons", crea un arreglo buit i arega-li "valor".
        -si "valor" no és una cadena buida, agrega "valor" al final de l'arreglo de cançons de l'àlbum corresponent.
    -Si "valor" no és una cadena buida i "propietat" no és igual a "cançons", assigna el valor del paràmetre
    "valor" a la propietat. Si la propietat no existeix, has de crear-la i assignar-li aquest valor.
*/

function actualitzarDisc(discos, id, propietat, valor){
    if(valor === ""){
        delete discos[id][propietat];
    }else if (propietat === "cançons"){
        discos[id][propietat] = discos[id][propietat] || [];
        discos[id][propietat].push(valor);
    }else{
        discos[id][propietat] = valor;
    }
}

console.log(coleccioDiscs[7853].titolAlbum);
actualitzarDisc(coleccioDiscs,7853,"titolAlbum","");
console.log(coleccioDiscs[7853].titolAlbum);

console.log(coleccioDiscs[5439].titolAlbum);
actualitzarDisc(coleccioDiscs,5439,"titolAlbum","Mamma Mia");
console.log(coleccioDiscs[5439].titolAlbum);

console.log(coleccioDiscs[5439].cançons);
actualitzarDisc(coleccioDiscs,5439,"cançons","Mamma Mia");
console.log(coleccioDiscs[5439].cançons);

console.log(coleccioDiscs[5439].artista);
actualitzarDisc(coleccioDiscs,5439,"artista","ABBA");
console.log(coleccioDiscs[5439].artista);
```
</div>

<br>
<br>
<br>

# While
<div class="defi">

```cs
var i = 0;
arreglo = [];

while (i<5){
    arreglo.push(i);
    i++
}
console.log(arreglo);

//---> [0, 1, 2, 3, 4]
```
</div>

## Exemple amb length
<div class="defi">

```cs
var i = 0;
nums = [2,3,4,5,6,8,10,34];

while (nums.length>4){
    nums.pop();
}
console.log(nums);
```
</div>

<br><br><br>

## Do-while

<div class="exemple">

```cs
var compt = 0;
do{
    console.log(compt);
    compt++;
} while (compt<5);

//---> 0 1 2 3 4
```
</div>



<br><br><br>

# For
<div class="defi">

```cs
var vect = [];

for (var i=0; i<10; i+=2){
    vect.push(i);
}
```
</div>

## For enrere
<div class="defi">

```cs
var vect = [];

for (var i=30; i>10; i-=2){
    vect.push(i);
}

```
</div>

## UPPER CASE
<div class="defi">

```cs
var llengues = ["Català", "castellà", "anglès"]

for (var i=0; i < llengues.length; i++){
    console.log(llengues[i].toUpperCase());
}

//---> CATALÀ, CASTELLÀ, ANGLÈS
```
</div>



<br><br><br>

# Ciclos Anidados
CICLES DINS D'ALTRES CICLES.

ARREGLOS QUE CONTENEN ALTRES ARREGLOS.

<div class="defi">

```cs
var vect = [[1,2,3],[4,5,6],[7,8,9]];

for (var i=0; i<vect.length; i++){
    console.log("Nova iteració")
    var vectAnidado = vect[i];
    for (var j=0 ; j<vectAnidado.length; j++){
        console.log(">>>> CICLE ANIDADO >>>> ELEMENT", vectAnidado[j], vect[i]);
    }
}


//---> Nova iteració
//---> >>>> CICLE ANIDADO >>>> ELEMENT 1 [ 1, 2, 3 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 2 [ 1, 2, 3 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 3 [ 1, 2, 3 ]
//--->  Nova iteració
//---> >>>>  CICLE ANIDADO >>>> ELEMENT 4 [ 4, 5, 6 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 5 [ 4, 5, 6 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 6 [ 4, 5, 6 ]
//---> Nova iteració
//---> >>>> CICLE ANIDADO >>>> ELEMENT 7 [ 7, 8, 9 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 8 [ 7, 8, 9 ]
//---> >>>> CICLE ANIDADO >>>> ELEMENT 9 [ 7, 8, 9 ]
```
</div>



<div class="exemple">

```cs
var contactes = [
    {
        "nom": "Nora",
        "cognom": "Garcia",
        "numero": "635456788",
        "preferencies": ["Pizza", "Programar"]
    },{
        "nom": "Harry",
        "cognom": "Potter",
        "numero": "654321987",
        "preferencies": ["Hoggwarts", "Magia"]
    },{
        "nom": "Sherlock",
        "cognom": "Holmes",
        "numero": "632154978",
        "preferencies": ["Misteris", "Violí"]
    }
];


function buscarPerfil(nom, propietat){
0    for(var i=0; i<contactes.length; i++){
        if(contactes[i].nom === nom ){
            return contactes[i][propietat] || "La propietat no existeix.";
            //No podem utilitzar .propietat xq és una variable
            //Si escrivíssim .propietat, el programa buscaria contactes.propietat i no trobaria res.
        }
    }
    return "El contacte no està a la llista."
}

console.log(buscarPerfil("Nora", "preferencies"));

console.log(buscarPerfil("Sherlock", "adressa"));

console.log(buscarPerfil("Bob", "numero"));

//---> [ 'Pizza', 'Programar' ]
//---> La propietat no existeix.
//---> El contacte no està a la llista.
```
</div>

<br><br><br>

# Números aleatoris

```cs
var numAleatori = Math.floor(Math.random()*20);
// floor retorna el número més gran que és menor o igual al nombre que li passem entre parèntesi.
// Math.random retorna un número decimal aleatori entre 0 i 1 així que el multipliquem i floor serà el que busqui l'enter que més se li ajusti.

```
FUNCIÓ PER NOMBRES ALEATORIS
<div class="exemple">

```cs
function generarEnterAleatori (limitSuperior){
    //Generem un enter aleatori entre 0 i el límit superior (sense incluir-lo).
    return Math.floor(Math.random()*limitSuperior);
}
```
</div>

EXEMPLE
<div class="defi">

```cs
function generarEnterAleatori (limitSuperior){
    return Math.floor(Math.random()*limitSuperior);
}

for (var i=0; i<10; i++){
    console.log(generarEnterAleatori(100));
}

//---> 89  38  12  26  20  22  93  11  96  99
```
</div>

<br><br><br>

## Números aleatoris EN UN RANG
<div class="exemple">

```cs
function rangAleatori (limitSuperior, limitInferior){
    return Math.floor(Math.random()*(limitSuperior-limitInferior+1))+limitInferior;
}
// En aquest cas el límit superior si que s'inclou en els possibles resultats
```
</div>


<br><br><br>

## Funció parseInt()
És una funció que converteix una cadena de caràcters a un enter

<div class="exemple">

```cs
console.log(parseInt("-4.5"));
console.log(parseInt("abc"));

//---> -4
//---> NaN
```
</div>

<div class="defi">

```cs
var a= parseInt("5");
var b= parseInt("7");

console.log(a+b);

//---> 12
```
</div>


# PARSEINT() amb base
Podem passar la base del sistema numèric a la funció PARSEINT().
<div class="exemple">

```cs
console.log(parseInt(110111,2));
//Podem passar el numero sense ser cadena de caràcters
// i el 2 representa la base numèrica.
```
</div>

<br><br><br>

# Operador condicional (ternari)
És un operador que ens permet compactar un operador en una sola línia.

<div class="exemple">

```cs
function minim(x,y){
    if(x<y){
        return x;
    } else{
        return y;
    } 
}


>>>>>> ÉS EQUIVALENT


function returnMinim(x,y){
    return x<y ? x : y;
    //si x<y és cert, retorna x. Si no és cert, retorna y.
}
```
</div>

<br><br><br>

# Múltiples Operadors Condicionals
<div class="exemple">

```cs
function compararNumeros(a,b){
    if (a==b){
        return "a i b són iguals";
    } else if(a>b) {
        return "a és més gran que b";
    } else {
        return "b és més gran que a";
    }
}

function comparaNum(a,b) {
    return a==b ? "a i b són iguals"
        : a>b ? "a és més gran que b"
        : "b és més gran que a";
}
```
</div>

<br><br><br>

# VAR vs LET
La diferència entre elles és que podem declarar la mateixa variable VAR tantes vegades com vulguem.



<div class="defi">

```cs
var global=1;

function funLocal (global){
    var local = 8;
    console.log("Local:", local);
    console.log("Global:", global); 
}

console.log(funLocal(global));  //--->>> 8, 1
console.log(global);  //--->>> 8
console.log(local); //--->>> Not defined. La variable està dins de la funció.
```
</div>

A més, la variable LET és més restrictiva pel que fa a variables locals i globals.
<div class="defi">

```cs
for (var i=0; i<3; i++)
    console.log(i);  //---> 0,1,2

console.log("Variable:" + i); //---> Variable:3
```
</div>

<div class="defi">

```cs
for (let i=0; i<3; i++)
    console.log(i);  //---> 0,1,2

console.log("Variable:" + i); //---> ReferenceError: i is not defined. Està fora del bucle on l'utilitzem. 
```
</div>

Si utilitzem les variables dins dels condicionals no hi ha problema.
<div class="defi">

```cs
var mostrar= false;


if(mostrar){
    let color= "verd";
    console.log("El meu color preferit és: " + color);
}else{
    let color= "blau";
    console.log("El color és: " + color);  //---> El color és: blau
}
```
</div>

<br><br><br>

# CONST

No podem modificar el seu valor una vegada ha estat adjudicat.

<div class="exemple">

```cs
const constant = 5;
console.log(constant); //---> 5


function calcularAreaCercle(radi){
    const PI=3.14;

    if(radi<0)  return undefined;

    return PI*(radi**2);
    //El valor de la constant PI no canviarà al llarg de tot el programa.
}


```
</div>

<br><br><br>

# Mutar arreglo declarat amb CONST
Podem modificar el valor individual de la constant CONST de la següent manera:

<div class="defi">

```cs
const arreglo = [0,1,2,3,4];
arreglo[0] = 5;
arreglo[1] = 6;
arreglo[2] = 7;

console.log(arreglo);
//---> [5, 6, 7, 3, 4]
```
</div>

<br><br><br>

# Crear ubn objecte IMMUTABLE

Amb l'opció '''Object.freeze()''' podem congelar l'objecte quan s'executa aquella línia.

<div class="exemple">

```cs
let colors={
    "verd": "#10e04b",
    "blau": "#1b50e0",
    "negre": "#000000",
    "blanc": "#ffffff"
};

Object.freeze(colors);

colors.groc = "#fff200";
//Ens hauria de sortir: TypeError: Cannot add property groc, object is not extensible.
//Ja que no se li poden afegir més propietats als colors despres de FREEZE.
colors.verd= "#345sg5";
//Ens hauria de sortir: TypeError: Cannot assign to read only property "verd" of object "#<Object>".
//Ja que no se li poden modificar les propietats després de FREEZE.
colors delete.verd;
colors.verd= "#345sg5";
//Ens hauria de sortir: TypeError: Cannot delete property "verd" of "#<Object>".
//Ja que no es poden eliminar propietats després de FREEZE.

console.log(colors);
//--->>> {verd: '#10e04b', blau: '#1b50e0',negre:'#000000', blanc: '#ffffff'}
```
</div>

<br><br><br>

# Funcions Fletxa

Ens permeten escriure funcions més conscises en JS.

S'utilitzen molt quan volem definir funcions anònimes; és a dir, quan no tenen un nom específic.

<div class="exemple">

```cs
const data = function() { //tenim una funció anònima que no rep cap paràmetre
    return new Date(); //retornem un objecte
}
//tot això se li assigna a una variable
```
</div>

Podem reescriure aquesta funció d'una altra manera.

Treiem la paraula clau Function i treiem els claudators i RETURN. Ho subtituïm per =>.

<div class="exemple">

```cs
const data = () => new Date();
```
</div>

<br><br>

<div class="defi">

```cs
const sumTres = function(x){
    return x+3;
}

//ÉS EQUIVALENT A

const sumaTres = (x) => x+3;
```
</div>


<br><br>

<div class="defi">

```cs
const concatenar = function(arreg1, arreg2){
    return arreg1.concat(arreg2);
}

//ÉS EQUIVALENT A

const concaternar = (arreg1, arreg2) => arreg1.concat(arreg2);
```
</div>


<br><br>
Com ho fem si la funció té més d'una línia.
<div class="defi">

```cs
const sumar = function(a, b){
    let num = 6;
    return a+b+num;
}

//ÉS EQUIVALENT A

const sumar = (a,b) => {
    let num = 6;
    return a+b+num;
};
```
</div>

<br><br><br>

# Valors per defecte per paràmetres
Podem assignar valors per defecte i després modificar-los.

<div class="exemple">

```cs
const incrementar = (num, valor=1) => num+valor;

console.log(incrementar(5)); //---> 6
// num passa a ser 5
console.log(incrementar(5, 3)); //---> 8
//es modifica el valor del paràmetre VALOR a 3
```
</div>

<br><br><br>

# Operador REST
Ens permet passar qualsevol nombre d'arguments a una funció i que aquests d'agrupin com un Arreglo.

<div class="exemple">

```cs
function mevaFuncio(a,b,c,d){
    console.log();
}

//ENLLOC DE a,b,c,d, posem: ...args
function mevaFuncio(...args){
    console.log(args);
}

mevaFuncio(1);//---> [1]
mevaFuncio(1,2);//---> [ 1, 2 ]
mevaFuncio("a",1,2);//---> [ 'a', 1, 2 ]


```
</div>

Podem demanar que faci altres coses com per exemple:
<div class="defi">

```cs
function mevaFuncio(...args){
    console.log(args);
}
mevaFuncio("a",1,2);
//---> 3
```
</div>

<br><br><br>

# Operador REDUCE
Es una funció que partint d'un Array ens retorna el seu valor acumulat.

<div class="exemple">

```cs
const sumar = (x,y,z) => {
    const args = [x,y,z];
    return args.reduce((a,b) => a+b, 0)
}

console.log(sumar(1,7,2,'a'));

//---> 10
//Retorna 10 perquè li estem dient que només prengui els 3 primers valors
```
</div>

Si volem que prengui un nombre indefinit d'arguments, podem escriure-ho de manera equivalent:

<div class="defi">

```cs
const sumar = (...args) => {
    return args.reduce((a,b) => a+b, 0)
}

console.log(sumar(1,7,2,'a'));
//---> 10a
```
</div>

<br><br><br>

# Operador SPREAD
Pren un arreglo i ho descomposa en els seus elements individuals.

<div class="exemple">

```cs
const numeros =[1,2,'r'];

function sumar(x,y,z){
    return x+y+z;
}

//Enlloc d'haver d'escriure TOTS els paràmetres
console.log(sumar(numeros[0],numeros[1],numeros[2]));
//Podem escriure
console.log(sumar(...numeros));

//---> 3r
```
</div>

<br><br><br>

# Sintaxi de destructuratzió

<div class="defi">

```cs
const coordenades = {
    x: 4,
    y: 6,
    z: 12
};

var x= coordenades.x;
var y= coordenades.y;
var z= coordenades.z;

//Podem escriure això en una sola línia de manera més ràpida
const {x,y,z} = coordenades;
```
</div>

<br><br><br>

# Sintaxi de destructuratzió: Objectes anidados

<div class="defi">

```cs
const usuari = {
    johnDoe:{
        edat: 27,
        correu: "johndoe@ex.com"
    }
};
const {johnDoe:{edat: edatDeLusuari, correu: correuDeLusuari}} = usuari;
//Estem declarant nous noms EDAT i CORREU i passen a ser les variables (edat i correu son propietats)
```
</div>


<div class="defi">

```cs
const PRONOSTIC_LOCAL = {
    "ahir": {
        minima: 61,
        maxima: 75
    },
    "avui": {
        minima: 64,
        maxima: 77
    },
    "dema": {
        minima: 68,
        maxima: 80
    }
};

const minimaAvui = PRONOSTIC_LOCAL.avui.minima;
const maximaAvui = PRONOSTIC_LOCAL.avui.maxima;

//Podem escriure-ho:

const {avui: {minima: minimaAvui, maxima: maximaAvui}} = PRONOSTIC_LOCAL;

console.log(minimaAvui, maximaAvui);
//---> 64 77
```
</div>

<br><br><br>

# Sintaxi de destructuratzió: Arreglos

Si volem assignar valors en diferents posicions, per exemple, zero, primera i quarta posició, podem fer:
<div class="exemple">

```cs
var a;
var b;
var c;

[a,b,,,c] = [0,1,2,3,4,5,6];

console.log(a,b,c);

//---> 0,1,4
```
</div>

Podem utilitzar la sintaxi de destructuració per canviar o intercanviar els valors de dues variables, per exemple:

<div class="exemple">

```cs
var a = 8;
var b = 3;

[a,b] = [b,a]

console.log("a = ", a,"  b = ", b);

//---> a =  3  b =  8
```
</div>

<br><br><br>

# Sintaxi de destructuratzió: Amb l'operador REST

Recordem que l'operador REST agrupa els arguments i forma un arreglo quan operem amb funcions.

<div class="defi">

```cs
var a;
var b;
var args;

[a,b,...args] = [1,2,3,4,5];

console.log(a,b);
console.log(args);
//---> 1 2
//---> [ 3, 4, 5 ]
```
</div>

Exemple de com eliminar elements d'una array amb REST
<div class="defi">

```cs
const arregloInicial = [1,2,3,4,5,6,7,8,9];

function eliminarTresPrimersElements(arreglo) {
    const [,,, ...nouArreglo] = arreglo;
    return nouArreglo;
}

const arregloFinal = eliminarTresPrimersElements(arregloInicial);
console.log(arregloFinal);
```
</div>

<br><br><br>

# Sintaxi de Desestructuració: Passar Objecte com Argument 

<div class="defi">

```cs
var nouPerfilClient = {
    nom: "Joe Doe",
    edat: 24,
    nacionalitat: "espanyola",
    ubicacio: "Espanya"
};

const actualitzarPerfil = (informacioDePerfil) => {
    const {nom, edat, nacionalitat, ubicacio} = informacioDePerfil;
    console.log(nom);
    console.log(edat);
};

actualitzarPerfil(nouPerfilClient);

// És equivalent a passar els paràmetres que volem agafar i cridar la variable que volem associar.

const actualitzarPerfil = ({nom, edat}) => {
    console.log(nom);
    console.log(edat);
};

actualitzarPerfil(nouPerfilClient);

```
</div>

EXEMPLE 2
<div class="defi">

```cs
const estadistiques = {
    max: 56.78,
    desviacioEstandard: 4.34,
    mitjana: 34.54,
    moda: 23.87,
    min: -0.75,
    promitg: 35.85
};

const meitat = (e) => (e.max +e.min)/2.0;

// És equivalent a 

const meitat = ({max, min}) => (max + min) / 2.0;
```
</div>

<br><br><br>

# Plantilles literals

<div class="exemple">

```cs

```
</div>