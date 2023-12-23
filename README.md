## Introducció a Biopython.

La teoria respecte Biopython es troba en aquest document:

https://docs.google.com/document/d/1v0BcVDdad613peyC_aMyqM0ehR33idG-AhkUf1WbU8Y/edit

## Com llegir fitxers .fasta amb la shell de Linux:

Molt fàcil!

```bash
grep -E '^\S+$' sequences.fa | awk '{printf "%s ", $0; getline; print $0}'
```

## Exercicis bloc 1.

Escriu un programa que llegeixi un fitxer FASTA indicat per codi:
1.- Imprimeixi un fitxer FASTA nou amb el complement invers = reverse complementary de cada seqüència.
2.- El contingut GC de cada seqüència.
3.- Descarrega’t el fitxer .fasta de la orquidea, prova el codi i analitza els resultats.
https://github.com/biopython/biopython/blob/master/Doc/examples/ls_orchid.fasta
4.- Millora el programa (si encara no ho has fet) i fes que si l’usuari introdueix un fitxer fasta pel terminal 
que imprimeixi el fasta del terminal, i si no ho ha fet, que avisi a l’usuari que la idea és que posi un fitxer fasta, 
però en comptes de sortir del programa que llegeixi un fasta passat per codi (el secuences.fa)
5.- Afegeix un mecanisme per verificar quines seqüències del fitxer FASTA només tinguin seqüències d'ADN vàlides i sense ambigüitats: 
(validant els caràcters) i ho mostri per pantalla. 

<em>Observació: Tot i que ja vam veure que ens podem trobar seqüències amb caràcters com la N 
(que indica que pot ser qualsevol àcid nucleic = qualsevol lletra) i és un caràcter vàlid en els fitxers fasta; no ens interessa tenir cadenes ambigües.</em>

## Activitat 
També és molt important recordar com llegir un fitxer .fasta de nucleotids i convertir-lo a proteïna; l‘objectiu de l’activitat és fer crear el codi que converteixi adn a proteïnes. 
Al final, aconsegueix que guardi el fitxer resultant en un altra fasta, que tingui el mateix nom excepte que els últims caràcters siguin “_newprot”.fasta

## Exercici 6.
Seguint amb el pas 5 (solució de l'exercici), fes un nou programa que tradueixi un seqüència d’ADN o un ARN a una de proteïnes. 
Al final, ha de guardar la proteïna en un altre fitxer que tingui el mateix nom juntament amb el text “_newprot”. 
La capçalera ha de ser la mateixa que el fasta de nucleòtids, afegint el text “, translated by Biopython”.
