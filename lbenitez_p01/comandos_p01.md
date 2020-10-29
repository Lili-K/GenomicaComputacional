# Comandos de la Práctica 01

## Liliana Benítez Salazar 

# Parte I.

** Respuesta 1: **
echo $SHELL 
/bin/bash.exe

** Respuesta 2: **
mkdir  data filtered raw_data meta scripts figures archive

** Respuesta 3: **
mv filtered ./data
mv raw_data ./data

** Respuesta 4: **
echo "El nombre de los diferentes directorios que creamos deben su nombre a los elementos básicos de todo proyecto bioinformáticos, este debe encontrarse en un directorio (carpeta) en donde se encuentre todo perfectamente bien documentado, esto con la finalidad de que en un futuro nuestro trabajo pueda ser reproducible.  1. Data: donde están contenidos los datos 2. Meta: donde se encuentran guardados los metadatos 3. Scrips: espacio para guardar los scripts empleados para correr un análisis. 4. Figure: contiene el código donde utilizado para las figuras de cierta publicación. 5. Archive: espacio para almacenar código que podríamos requerir en un futuro." >> ./lbenitez_p01/comandos_p01

# Parte II.

** Respuesta 1: **
cd ./GenomicaComputacional/lbenitez_p01/scripts
chmod +x delay.sh

** Respuesta 2: **
ls -lh
total 1
-rwxr-xr-x    1 Lilana   UsersGrp      93 Oct 23 23:21 delay.sh

** Respuesta 3: **
echo "Después de la Parte I. necesito un descanso de exactamente 30 segundos."
sleep 30 
echo "Ya puedo continuar! "

** Respuesta 4: **
sleep 300 &
[1] 1242
ps
 1242    1036    1242       5256  pty0        1002 01:07:21 /usr/bin/bash
     1243    1242    1242       4332  pty0        1002 01:07:21 /usr/bin/busybox
     1246    1036    1246       5136  pty0        1002 01:07:37 /usr/bin/ps
kill 1242
[1]+  Terminated              _bbf sleep 300

# Parte III.

** Respuesta 1: **
home/GenomicaComputacional/lbenitez_p01/meta
touch SarsCov-2.txt
echo "El Sars-Cov2 es un betacoronavirus de RNA con marco de lectura abierto que codifica para proteínas no estructurales y estructurales, como S1 y S2 de membrana. Estudios filogéneticos  han encontrado una relación de Sars-Cov2 con coronavirus de murciélagos. El RNA del coronavirus se encuentra envuelto en una cápside, de su membrana sobresalen espículas glicosiladas. El subdominio S2 de la proteína S es responsable de la unión al receptor de células blanco.Entre los receptores está  la enzima Convertidora de Angiotensina 2. Como conclusión es de suma importancia conocer la estructura molecular del virus, ya que son aspectos clave para el desarrollo de un vacuna. Un ejemplo de vacuna es la que expresa  las proteínas la espicula mezcladas con un adyuvante."

** Respuesta 2: **
/home/Lilana/Desktop 
mv sequence.fasta sarscov2_genome.fasta
mv sequence.gff3 sarvscov2_genome.gff3
mv sequence.fasta splike_c.faa
mv 'sequence. (1)'.fasta splike_b.faa
mv 'sequence. (2)'.fasta splike_a.faa

Dropbox.lnk                         genes_coli - Shortcut.lnk
GitHub Desktop.lnk                  genes_coli.txt
IGC - IGC.tsv - Shortcut.lnk        genoma1.fasta - Shortcut.lnk
Lili.txt                            n.txt
MobaXterm_home_20201014_201041.rtf  negri.txt
New folder                          negrita.txt
README.md - Shortcut.lnk            negrito.txt
Spotify.lnk                         sarscov2_genome.fasta
Thumbs.db                           sarvscov2_genome.gff3
archivo.txt                         splike_a.faa
comandos_p01.md                     splike_b.faa
desktop.ini                         splike_c.faa
gen (1).fna - Shortcut.lnk          teamo.html
gen.fna - Shortcut.lnk
   
mv sarscov2_genome.fasta sarscov2_assembly.fasta.gz sarvscov2_genome.gff3 splike_a.faa splike_b.faa splike_c.faa SRR10971381_R1.fastq.gz SRR10971381_R2.fastq.gz ./GenomicaComputacional/lbenitez_p01/data/raw_data/
                                                                            
total 7458
-rw-r--r--    1 Lilana   UsersGrp    7.2M Oct 24 15:45 SRR10971381_R1.fastq.gz
-rw-r--r--    1 Lilana   UsersGrp    7.2M Oct 24 15:45 SRR10971381_R2.fastq.gz
-rw-r--r--    1 Lilana   UsersGrp   11.5K Oct 24 15:45 sarscov2_assembly.fasta.gz
-rw-r--r--    1 Lilana   UsersGrp   29.7K Oct 24 13:33 sarscov2_genome.fasta
-rw-r--r--    1 Lilana   UsersGrp   14.3K Oct 24 13:34 sarvscov2_genome.gff3
-rw-r--r--    1 Lilana   UsersGrp    1.3K Oct 24 15:50 splike_a.faa
-rw-r--r--    1 Lilana   UsersGrp    1.3K Oct 24 15:50 splike_b.faa
-rw-r--r--    1 Lilana   UsersGrp    1.3K Oct 24 15:49 splike_c.faa

# Parte IV.

** Respuesta 1: **
ln -s /home/GenomicaComputacional/lbenitez_p01/data/raw_data splike_a.faa /home/GenomicaComputacional/lbenitez_p01/data/filtered
ln -s /home/GenomicaComputacional/lbenitez_p01/data/raw_data splike_b.faa /home/GenomicaComputacional/lbenitez_p01/data/filtered                                                                          
ln -s /home/GenomicaComputacional/lbenitez_p01/data/raw_data splike_c.faa /home/GenomicaComputacional/lbenitez_p01/data/filtered
ls -lth
total 4
lrwxrwxrwx    1 Lilana   UsersGrp      12 Oct 28 00:42 splike_c.faa -> splike_c.faa
lrwxrwxrwx    1 Lilana   UsersGrp      12 Oct 28 00:42 splike_b.faa -> splike_b.faa
lrwxrwxrwx    1 Lilana   UsersGrp      54 Oct 28 00:34 raw_data -> /home/GenomicaComputacional/lbenitez_p01/data/raw_data
lrwxrwxrwx    1 Lilana   UsersGrp      12 Oct 28 00:34 splike_a.faa -> splike_a.faa
-rw-r--r--    1 Lilana   UsersGrp    4.0K Oct 27 22:57 glycoproteins.faa
                                                        
** Respuesta 2: **
/home/GenomicaComputacional/lbenitez_p01/data/filtered
touch glycoproteins.faa
  

** Respuesta 3: **
head -n 1 splike_a.faa
>pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein

head -n 1 splike_b.faa
>pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein

head -n 1 splike_c.faa
>pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein

** Respuesta 4: **
less splike_a.faa splike_b.faa splike_c.faa  >> ./../filtered/glycoproteins.faa
cd ./..
cd ./filtered
cat glycoproteins.faa

>pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein
MGILPSPGMPALLSLVSLLSVLLMGCVAETGTQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHST
QDLFLPFFSNVTWFHAIHVSGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVN
NATNVVIKVCEFQFCNDPFLGVYYHKNNKSWMESEFRVYSSANNCTFEYVSQPFLMDLEGKQGNFKNLRE
FVFKNIDGYFKIYSKHTPINLVRDLPQGFSALEPLVDLPIGINITRFQTLLALHRSYLTPGDSSSGWTAG
AAAYYVGYLQPRTFLLKYNENGTITDAVDCALDPLSETKCTLKSFTVEKGIYQTSNFRVQPTESIVRFPN
ITNLCPFGEVFNATRFASVYAWNRKRISNCVADYSVLYNSASFSTFKCYGVSPTKLNDLCFTNVYADSFV
IRGDEVRQIAPGQTGKIADYNYKLPDDFTGCVIAWNSNNLDSKVGGNYNYLYRLFRKSNLKPFERDISTE
IYQAGSTPCNGVEGFNCYFPLQSYGFQPTNGVGYQPYRVVVLSFELLHAPATVCGPKKSTNLVKNKCVNF
NFNGLTGTGVLTESNKKFLPFQQFGRDIADTTDAVRDPQTLEILDITPCSFGGVSVITPGTNTSNQVAVL
YQDVNCTEVPVAIHADQLTPTWRVYSTGSNVFQTRAGCLIGAEHVNNSYECDIPIGAGICASYQTQTNSP
SGAGSVASQSIIAYTMSLGAENSVAYSNNSIAIPTNFTISVTTEILPVSMTKTSVDCTMYICGDSTECSN
LLLQYGSFCTQLNRALTGIAVEQDKNTQEVFAQVKQIYKTPPIKDFGGFNFSQILPDPSKPSKRSFIEDL
LFNKVTLADAGFIKQYGDCLGDIAARDLICAQKFNGLTVLPPLLTDEMIAQYTSALLAGTITSGWTFGAG
AALQIPFAMQMAYRFNGIGVTQNVLYENQKLIANQFNSAIGKIQDSLSSTASALGKLQDVVNQNAQALNT
LVKQLSSNFGAISSVLNDILSRLDPPEAEVQIDRLITGRLQSLQTYVTQQLIRAAEIRASANLAATKMSE
CVLGQSKRVDFCGKGYHLMSFPQSAPHGVVFLHVTYVPAQEKNFTTAPAICHDGKAHFPREGVFVSNGTH
WFVTQRNFYEPQIITTDNTFVSGNCDVVIGIVNNTVYDPLQPELDSFKEELDKYFKNHTSPDVDLGDISG
INASVVNIQKEIDRLNEVAKNLNESLIDLQELGKYEQYIKGSGRENLYFQGGGGSGYIPEAPRDGQAYVR
KDGEWVLLSTFLGHHHHHHHH

>pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein
MGILPSPGMPALLSLVSLLSVLLMGCVAETGTQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHST
QDLFLPFFSNVTWFHAIHVSGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVN
NATNVVIKVCEFQFCNDPFLGVYYHKNNKSWMESEFRVYSSANNCTFEYVSQPFLMDLEGKQGNFKNLRE
FVFKNIDGYFKIYSKHTPINLVRDLPQGFSALEPLVDLPIGINITRFQTLLALHRSYLTPGDSSSGWTAG
AAAYYVGYLQPRTFLLKYNENGTITDAVDCALDPLSETKCTLKSFTVEKGIYQTSNFRVQPTESIVRFPN
ITNLCPFGEVFNATRFASVYAWNRKRISNCVADYSVLYNSASFSTFKCYGVSPTKLNDLCFTNVYADSFV
IRGDEVRQIAPGQTGKIADYNYKLPDDFTGCVIAWNSNNLDSKVGGNYNYLYRLFRKSNLKPFERDISTE
IYQAGSTPCNGVEGFNCYFPLQSYGFQPTNGVGYQPYRVVVLSFELLHAPATVCGPKKSTNLVKNKCVNF
NFNGLTGTGVLTESNKKFLPFQQFGRDIADTTDAVRDPQTLEILDITPCSFGGVSVITPGTNTSNQVAVL
YQDVNCTEVPVAIHADQLTPTWRVYSTGSNVFQTRAGCLIGAEHVNNSYECDIPIGAGICASYQTQTNSP
SGAGSVASQSIIAYTMSLGAENSVAYSNNSIAIPTNFTISVTTEILPVSMTKTSVDCTMYICGDSTECSN
LLLQYGSFCTQLNRALTGIAVEQDKNTQEVFAQVKQIYKTPPIKDFGGFNFSQILPDPSKPSKRSFIEDL
LFNKVTLADAGFIKQYGDCLGDIAARDLICAQKFNGLTVLPPLLTDEMIAQYTSALLAGTITSGWTFGAG
AALQIPFAMQMAYRFNGIGVTQNVLYENQKLIANQFNSAIGKIQDSLSSTASALGKLQDVVNQNAQALNT
LVKQLSSNFGAISSVLNDILSRLDPPEAEVQIDRLITGRLQSLQTYVTQQLIRAAEIRASANLAATKMSE
CVLGQSKRVDFCGKGYHLMSFPQSAPHGVVFLHVTYVPAQEKNFTTAPAICHDGKAHFPREGVFVSNGTH
WFVTQRNFYEPQIITTDNTFVSGNCDVVIGIVNNTVYDPLQPELDSFKEELDKYFKNHTSPDVDLGDISG
INASVVNIQKEIDRLNEVAKNLNESLIDLQELGKYEQYIKGSGRENLYFQGGGGSGYIPEAPRDGQAYVR
KDGEWVLLSTFLGHHHHHHHH

>pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein
MGILPSPGMPALLSLVSLLSVLLMGCVAETGTQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHST
QDLFLPFFSNVTWFHAIHVSGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVN
NATNVVIKVCEFQFCNDPFLGVYYHKNNKSWMESEFRVYSSANNCTFEYVSQPFLMDLEGKQGNFKNLRE
FVFKNIDGYFKIYSKHTPINLVRDLPQGFSALEPLVDLPIGINITRFQTLLALHRSYLTPGDSSSGWTAG
AAAYYVGYLQPRTFLLKYNENGTITDAVDCALDPLSETKCTLKSFTVEKGIYQTSNFRVQPTESIVRFPN
ITNLCPFGEVFNATRFASVYAWNRKRISNCVADYSVLYNSASFSTFKCYGVSPTKLNDLCFTNVYADSFV
IRGDEVRQIAPGQTGKIADYNYKLPDDFTGCVIAWNSNNLDSKVGGNYNYLYRLFRKSNLKPFERDISTE
IYQAGSTPCNGVEGFNCYFPLQSYGFQPTNGVGYQPYRVVVLSFELLHAPATVCGPKKSTNLVKNKCVNF
NFNGLTGTGVLTESNKKFLPFQQFGRDIADTTDAVRDPQTLEILDITPCSFGGVSVITPGTNTSNQVAVL
YQDVNCTEVPVAIHADQLTPTWRVYSTGSNVFQTRAGCLIGAEHVNNSYECDIPIGAGICASYQTQTNSP
SGAGSVASQSIIAYTMSLGAENSVAYSNNSIAIPTNFTISVTTEILPVSMTKTSVDCTMYICGDSTECSN
LLLQYGSFCTQLNRALTGIAVEQDKNTQEVFAQVKQIYKTPPIKDFGGFNFSQILPDPSKPSKRSFIEDL
LFNKVTLADAGFIKQYGDCLGDIAARDLICAQKFNGLTVLPPLLTDEMIAQYTSALLAGTITSGWTFGAG
AALQIPFAMQMAYRFNGIGVTQNVLYENQKLIANQFNSAIGKIQDSLSSTASALGKLQDVVNQNAQALNT
LVKQLSSNFGAISSVLNDILSRLDPPEAEVQIDRLITGRLQSLQTYVTQQLIRAAEIRASANLAATKMSE
CVLGQSKRVDFCGKGYHLMSFPQSAPHGVVFLHVTYVPAQEKNFTTAPAICHDGKAHFPREGVFVSNGTH
WFVTQRNFYEPQIITTDNTFVSGNCDVVIGIVNNTVYDPLQPELDSFKEELDKYFKNHTSPDVDLGDISG
INASVVNIQKEIDRLNEVAKNLNESLIDLQELGKYEQYIKGSGRENLYFQGGGGSGYIPEAPRDGQAYVR
KDGEWVLLSTFLGHHHHHHHH


** Respuesta 5: **
mv splike_a.faa ./../../archive
mv splike_b.faa ./../../archive
mv splike_c.faa ./../../archive

Lo que pasa con las ligas simbolicas al cambiar los archivos de ruta es que se rompen. 


** Respuesta 6: **
head -n 3 sarscov2_genome.fasta
>NC_045512.2 Severe acute respiratory syndrome coronavirus 2 isolate Wuhan-Hu-1, complete genome
ATTAAAGGTTTATACCTTCCCAGGTAACAAACCAACCAACTTTCGATCTCTTGTAGATCTGTTCTCTAAA
CGAACTTTAAAATCTGTGTGGCTGTCACTCGGCTGCATGCTTAGTGCACTCACGCAGTATAATTAATAAC

gunzip sarscov2_assembly.fasta.gz
head -n 3 sarscov2_assembly.fasta
>NODE_1_length_264_cov_161.042781
CACAAATCTTAACACTCTTCCCTACACGACGCTCTTCCGATCTACGCCGGGCCATTCGTA
CGAACCGATACCTGTGGTAAAGGGTCCTACTGTATGGTGGTACACGAGTAGTAGCAAATG

** Respuesta 7: **

** Respuesta 8: **
gunzip SRR10971381_R2.fastq.gz
head -n 12 SRR10971381_R2.fastq
@SRR10971381.512_2
CGTGGAGTATGGCTACATACTACTTATTTGATGAGTCTGGTGAGTTTAAAGTGGCTTCACATATGTATTGTTCTTTCTAC                                         CCTCCAGATGAGGATGAAGAAGAAGGTGATTGTGAAGAAGAAGAGTTTGAGCCATCAACTCAATATGAGT
+
/FFFA/A/FFFF66FFFFFF/FF/FFFFFFFFFFFFF/AFFF6FFFA6FFFFF/FFFFFFFFFFFFFFFFFF/FF/FFFF                                         FA/FFF/FFF/A/AFA/FFFFF/=F/F/F/AFAFF//A/AFF//FFAF/FFF=FFAFFFA/A/6=///==
@SRR10971381.556_2
TTTGTAAAAATAAAATAAAAAAAATAAAAATAATATATTAAAAAAAGATAAATAAAAAAATGAACAATTAATAAAAAAAA                                         AAAAAAAAAAAAATTAAAAAAAAAAAAAAAAAAAATAAAAAAAAAAAAAAATAAAAAAAAAATTATAAAA
+
6AFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF/FFFAFFFFFF/FFA/FF=F//=FF/FFFFFFFF                                         FFFFFA/FFFF/FF/FA//F/FFFFFFA/=FFFFF/FFFF/F=FFFAFF///FFFFA/FF/6//////=/
@SRR10971381.1428_2
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
+
FFFFFFFFFFFFAFFFAFFFFFF6A//F//FFF

Uno de los patrones que me podría ayudar a contar el número de secuencias, podría ser el @, ya que antes de cada secuencia se encuentra este caracter, junto con otros identificadores.
grep '@' SRR10971381_R2.fastq | wc -l


** Respuesta 9: **
El formato .faa contiene secuencias de proteínas, el formato fastqc indica que es un formato “FastA”, el cual es un formato estandar de texto para secuencias de DNA o RNA, este segundo formato contiene además "puntajes de calidad" de la secuencia y comienzan con un @ y el ID de la sequencia, la siguientes líneas contienen la secuencia, las posteriores contienen e caracter de + y las últimas líneas con los puntajes de calidad. Finalmente, los archivos fasta contienen secuencias representadas con texto y comienzan con un >.

** Respuesta 10: **
La diferencia entre less y less -S: Ambos nos muestran el contenido de los archivos , sin embargo less -S nos muestra el contenido de una manera más ordenada, alinea diferentes patrones de una linea en diferentes columnnas. 

** Respuesta 11: **
cut -f3 sarscov2_genome.gff3 | grep 'gene'
gene
gene
gene
gene
gene
gene
gene
gene
gene
gene
gene

cut -f3 sarscov2_genome.gff3 | grep 'gene' | wc -l
11

La diferencia entre genes y CDS es que CDS se refiere a las secuencias codificantes, es decir, las que codifican para un gen.

# Ejercicio extra



                