# terminal_2

## Abra una terminal con un sistema operativo basado en linux para realizar estos ejercicios básicos.

### Trabajo con archivos .fastq en _servidor_:

1.- Identifique en directorio donde se encuentra trabajando con el comando `pwd`. Luego acceda al directorio de trabajo donde están sus muestras (le indicará el profesor).

2.- Observe si hay archivos y/u otros directorios con el comando `ll`.

3.- Con el comando `ls -lh` vea nuevamente qué hay en el directorio. Puede ver que están casi los mismos archivos pero aparecen más detalles.

4.- Fíjese que las muestras de metagenomas están numeradas. Por ejemplo, el archivo tGRL10497_1_CGATGT_L001_R1_001.fastq.gz pertenece al metagenoma 1.
Ese archivo ya tiene las lecturas (reads) procesadas por calidad (por eso la t al inicio del nombre de archivo) y corresponde al primer archivo de lecturas de la secuenciación (indicado por R1).
El archivo tGRL10497_1_CGATGT_L001_R2_001.fastq.gz es el que tiene el otro par.

Entonces los archivos Forward y Reverse son tGRL10497_1_CGATGT_L001_R1_001.fastq.gz y tGRL10497_1_CGATGT_L001_R2_001.fastq.gz, respectivamente.

Estos archivos .fastq están comprimidos, por eso aparece .gz al final.

5.- Descomprima los archivos R1 de un único metagenoma con el comando programa gunzip (escriba `gunzip -h`). Debe usar el comando `gunzip -d -k -c`, por ejemplo:

`gunzip -d -k -c tGRL10497_1_CGATGT_L001_R1_001.fastq.gz > tGRL10497_1_CGATGT_L001_R1_001.fastq`. Este comando permite descomprimir el archivo y escribirlo sin .gz

6.- Una vez que tenga todos los R1 de un único metagenoma descomprimidos, debe concatenarlos con `cat`. 

Por ejemplo: `cat tGRL10497_1_CGATGT_L001_R1_001.fastq tGRL10497_1_CGATGT_L001_R1_002.fastq > cat_R1_metagenoma_1.fastq`.

## Es muy importante que respete el orden de los numeros, es decir, concatene el 1 primero, luego el 2, etc.

7.- Elimine los archivos .fastq que descomprimió. OJO, SOLO LOS QUE DESCOMPRIMIÓ, NO EL QUE ACABA DE CONCATENAR NI LOS COMPRIMIDOS. Use el comando `rm`.

Por ejemplo: `rm tGRL10497_1_CGATGT_L001_R1_001.fastq`

8.- Comprima el concatenado con el comando `gunzip`.

Por ejemplo: `gunzip cat_R1_metagenoma_1.fastq`

9.- Repita el proceso con el segundo del par (R2).

10.- Repita el proceso para cada uno de sus metagenomas. El producto final es un par de archvios para cada metagenoma:

cat_R1_metagenoma_1.fastq.gz cat_R2_metagenoma_1.fastq.gz
cat_R1_metagenoma_2.fastq.gz cat_R2_metagenoma_2.fastq.gz
cat_R1_metagenoma_3.fastq.gz cat_R2_metagenoma_3.fastq.gz

¡Felicitaciones! Tiene sus archivos listos para trabajar en [PhyloFlash](http://hrgv.github.io/phyloFlash/).

### Trabajo con PhyloFLash

11.- `phyloFlash.pl -lib metagenoma_x -CPUs 10 -dbhome /media/ddbb/pf/138.1 -almosteverything -read1 reads_F.fq.gz -read2 reads_R.fq.gz`

`-lib` *NAME*
            Library *NAME* to use for output file. The name must be one word
            comprising only letters, numbers and "_" or "-" (no whitespace
            or other punctuation).
            
`-taxlevel` *N*
            Level in the taxonomy string to summarize read counts per taxon.
            Numeric and 1-based (i.e. "1" corresponds to "Domain").

            Default: 4 ("Order")
