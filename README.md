# Pràctica 1: Cerca amb restriccions

Pol Pugibet Martinez - 1630568, Laia Rubio Castro - 1600830, Marc Serra Ortega - 1551550
Grup GM12:30_1

**Coneixement Raonament i Incertesa**
Grau en Enginyeria Informàtica
Escola d’Enginyeria

## Índex

1. Introducció
2. Solució proposada
   - Implementació inicial
   - Nivell C - Crossword puzzle (backtracking)
   - Nivell B - Crossword puzzle (forward checking)
3. Problemes sorgits
4. Conclusions i millores

## Introducció

Aquesta pràctica aborda el problema de la cerca amb restriccions, que implica omplir un tauler de mots encreuats amb un conjunt de paraules. S'han assolit objectius com l'aplicació de tècniques de cerca amb satisfacció de restriccions, l'ús de l'algorisme de backtracking amb forward checking, i la validació dels resultats. A continuació, expliquem la solució proposada en detall.

## Solució proposada

### Implementació inicial

La implementació inicial va implicar la càrrega de dades i la cerca de variables en el tauler i la creació d'un diccionari. Aquestes són algunes de les funcions clau:

- `loadCrossword(file)`: Carrega les paraules del tauler.
- `loadDictionary(file)`: Carrega les paraules del diccionari.

La cerca de variables es realitza amb les següents funcions:

- `cercaVariablesHoritzontal(taulell, variables)`: Troba les paraules consecutives horitzontals.
- `cercaVariablesVertical(taulell, variables)`: Troba les paraules consecutives verticals.
- `cercaVariables(taulell, variables)`: Combinació de les dues funcions anteriors.
- `calculaPosicionsVariable(variable)`: Calcula les possibles posicions d'una paraula en el tauler.

### Nivell C - Crossword puzzle (backtracking)

En aquest nivell, vam aplicar l'algorisme de backtracking per resoldre el tauler de mots encreuats. Abans de la implementació, vam definir les variables, el domini i les restriccions del problema. Hem utilitzat una estratègia per reduir la profunditat mitjana de les branques, ordenant les variables segons el nombre d'interseccions.

### Nivell B - Crossword puzzle (forward checking)

En aquest nivell, vam implementar el backtracking amb forward checking, una tècnica que elimina les solucions invàlides abans de l'exploració. A més a més, vam crear un diccionari de dominis per a millorar l'eficiència de la resolució.

## Problemes sorgits

L'adaptació dels models al nostre cas va ser el principal repte. Entendre les restriccions i la complexitat del problema va ser fonamental. També vam intentar implementar el MRV (Menor Valor Restringit) però no va ser eficient i vam deixar d'utilitzar-lo.

## Conclusions i millores

Aquesta pràctica ens ha familiaritzat amb els algorismes de cerca, i hem après a aplicar-los en un cas real. En el futur, podriem centrar-nos a millorar la qualitat del codi, tot i que hem aconseguit una bona complexitat algorítmica.
