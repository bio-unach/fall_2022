#terminal_1

##Abra una terminal con un sistema operativo basado en linux para realizar estos ejercicios básicos.

###Trabajo en _directorios_:

1.- Identifique en directorio donde se encuentra trabajando con el comando `pwd`. Este comando le dice dónde usted está y qué _ruta_ lleva a ese lugar.
La _ruta_ es la serie de carpetas o directorios que están antes. Por ejemplo: /carpeta1/carpeta2. Lo más probable es que en su caso diga /home/usuario,
siendo _usuario_ su nombre de usuario.
2.- Observe si hay archivos y/u otros directorios con el comando `ll`.
3.- Con el comando `ls -lh` vea nuevamente qué hay en el directorio. Puede ver que están casi los mismos archivos pero aparecen más detalles.
4.- Haga un nuevo directorio con el comando `mkdir` (puede darle el nombre que desee, por ejemplo `mkdir tfc`). 
**NO** escriba usando mayúsculas ni espacios, por ejemplo, si llama a su directorio `mkdir tfc 2022` tendrá problemas para que los programas de bioinformática
identifiquen ese directorio. Mejor escriba `mkdir tfc_2022`.
5.- Ingrese al directorio que acaba de hacer con el comando `cd`. Siguiendo con el ejemplo anterior, sería `cd tfc`.

###Trabajo básico con archivos en formato fasta

6.- Estando **dentro** del directorio que acaba de hacer, abra el editor de texto plano ***nano*** con el comando `nano`.
Esto abrirá, _en la misma terminal de linux_ una hoja nueva para escribir.
7.- Copie la siguiente secuencia de aminoácidos de una [proteína del ribosoma de la bacteria llamada _Borrelia anserina_](https://www.ncbi.nlm.nih.gov/protein/AHX39227.1?report=fasta) stá escrita en formato fasta):

8.- Pegue esta secuencia en la terminal donde tiene abierto ***nano***.
9.- Guarde el archivo presionando los botones `Ctrl`+`o` (control y la letra o).
El programa ***nano*** le pedirá dar un nombre a este archivo, escriba _miproteina.fasta_ (sin tildes). Luego presione el botón `Enter` de su teclado.
¡Felicitaciones! Ha guardado su primer gen en formato fasta, en este caso una proteína.
Nota: El formato fasta es muy sencillo, se compone de un _header_ y una secuencia (combinación de letras).
El _header_ (del inglés "encabezado") indica el nombre de la secuencia, y en la línea de abajo va la secuencia misma.
10. Repita desde el número 7 con la seguiente [secuencia de DNA](https://www.ncbi.nlm.nih.gov/nuccore/NR_024570.1/?report=fasta) ribosomal de la bacteria
_Escherichia coli_. Dele el nombre de _midna.fasta_.
¡Felicitaciones! Ha guardado su segundo gen en formato fasta, en este caso es una secuencia de DNA.
