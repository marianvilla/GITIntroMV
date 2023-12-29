# GITIntroMV
Estamos aprendiendo las bases iniciales para crear un proyecto en Github


### ¿Qué es Git y GitHub?</h3>

GIT es un sistema ya instalado en tu computadora, que nos permite tener distintas versiones de un proyecto en el que estemos trabajando, pudiendo tener el archivo del proyecto y luego otras versiones que son archivos para probar cosas, y qué los iremos testeando para ver si lo añadimos al archivo principal. Esto sirve mucho cuándo hay más de una persona trabajando en el proyectos, aumentando la productividad y la eficiencia. Por último, GIT se ejecuta en la terminal de tu computadora, y se utiliza a través de comandos, como merge, pull, add, commit.
Por otra parte, GitHub es una plataforma a la cual puedes subir a través de la nube (Internet) con el cual podemos subir nuestros proyectos y sus versiones que tenemos con Git.

### **¿Por qué usar un sistema de control de versiones como Git?**

Un sistema de control de versiones como Git nos ayuda a guardar el historial de cambios y crecimiento de los archivos de nuestro proyecto.

En realidad, los cambios y diferencias entre las versiones de nuestros proyectos pueden tener similitudes, algunas veces los cambios pueden ser solo una palabra o una parte específica de un archivo específico. Git está optimizado para guardar todos estos cambios de forma atómica e incremental, o sea, aplicando cambios sobre los últimos cambios, estos sobre los cambios anteriores y así hasta el inicio de nuestro proyecto.

El comando para iniciar nuestro repositorio, o sea, indicarle a Git que queremos usar su sistema de control de versiones en nuestro proyecto, es git init.

El comando para que nuestro repositorio sepa de la existencia de un archivo o sus últimos cambios es git add. Este comando no almacena las actualizaciones de forma definitiva, solo las guarda en algo que conocemos como “Staging Area” (no te preocupes, lo entenderemos más adelante).

El comando para almacenar definitivamente todos los cambios que por ahora viven en el staging área es git commit. También podemos guardar un mensaje para recordar muy bien qué cambios hicimos en este commit con el argumento -m "Mensaje del commit".

Por último, si queremos mandar nuestros commits a un servidor remoto, un lugar donde todos podamos conectar nuestros proyectos, usamos el comando git push.


Objetivos del curso:
-Instalar Git
-Crear un repositorio local (Experimentar) (Master local)
-Crear repositorio remoto (Compartir en la red)(Master remoto)

git init- inicializa el repositorio de git. Empieza en tu carpeta un repositorio para guardar los cambios.
git add . – Agrega todos los cambios en todos los archivos al área de staging
git status – Para ver el estado de la BD si se han hecho cambios, pero no se han agregado, ahí saldrá. Muestra el estado de tu repositorio
git show - Muestra todos los cambios históricos hechos y sus detalles (qué cambió, cuándo y quién los hizo). Muestra el histórico de los cambios hechos.
git commit: Envía los últimos cambios del archivo a la base de datos del sistema de control de versiones. Una buena práctica al usar este comando es añadir -m; al hacer esto, podemos escribir un mensaje que nos permita recordar los cambios que hicimos en ese momento.
git push -envía los cambios al repositorio remoto
git push origin <nombre_rama>: Sube la rama “nombre_rama” al servidor remoto.
git pull -Agrega los cambios del commit más nuevo al repositorio local
git log “nombre del archivo” : Muestra el historial de ese archivo. git log <nombre_archivo>: Muestra todo el historial del archivo.
git fetch: Descarga los cambios realizados en el repositorio remoto.
git merge <nombre_rama>: Impacta en la rama en la que te encuentras parado, los cambios realizados en la rama “nombre_rama”.
git checkout -b <nombre_rama_nueva>: Crea una rama a partir de la que te encuentres parado con el nombre “nombre_rama_nueva”, y luego salta sobre la rama nueva, por lo que quedas parado en esta última.
git checkout -t origin/<nombre_rama>: Si existe una rama remota de nombre “nombre_rama”, al ejecutar este comando se crea una rama local con el nombre “nombre_rama” para hacer un seguimiento de la rama remota con el mismo nombre.
git branch: Lista todas las ramas locales.
git branch -a:Lista todas las ramas locales y remotas.
git branch -d <nombre_rama>: Elimina la rama local con el nombre “nombre_rama”.
git push origin <nombre_rama>: Commitea los cambios desde el branch local origin al branch “nombre_rama”.
git remote prune origin: Actualiza tu repositorio remoto en caso que algún otro desarrollador haya eliminado alguna rama remota.
git reset --hard HEAD: Elimina los cambios realizados que aún no se hayan hecho commit.
git revert <hash_commit>: Revierte el commit realizado, identificado por el “hash_commit”.
Cuando se habla de “quedar parado”, se refiere a donde estás posicionado, dónde o en qué ruta estás realizando los comandos en la terminal.

Un editor de código es una herramienta que nos brinda muchas ayudas para escribir código, algo así como un bloc de notas muy avanzado. Los editores más populares son VSCode, Sublime Text y Atom, pero no necesariamente debes usar alguno de estos para continuar con el curso.

Tipos de archivos y sus diferencias:

Archivos de Texto (.txt): Texto plano normal y sin nada especial. Lo vemos igual sin importar dónde lo abramos, ya sea con el bloc de notas o con editores de texto avanzados.
Archivos RTF (.rtf): Podemos guardar texto con diferentes tamaños, estilos y colores. Pero si lo abrimos desde un editor de código, vamos a ver que es mucho más complejo que solo el texto plano. Esto es porque debe guardar todos los estilos del texto y, para esto, usa un código especial un poco difícil de entender y muy diferente a los textos con estilos especiales al que estamos acostumbrados.
Archivos de Word (.docx): Podemos guardar imágenes y texto con diferentes tamaños, estilos o colores. Al abrirlo desde un editor de código podemos ver que es código binario, muy difícil de entender y muy diferente al texto al que estamos acostumbrados. Esto es porque Word está optimizado para entender este código especial y representarlo gráficamente.

Conceptos bàsicos para trabajar con Git y dentro de un grupo de desarrolladores:

Repository: Donde se almacena todo el proyecto, el cual puede vivir tanto en local como en remoto. El repositorio guarda un historial de versiones y, más importante, de la relación de cada versión con la anterior para que pueda hacerse el árbol de versiones con las diferentes ramas.

Fork: Si en algún momento queremos contribuir al proyecto de otra persona, o si queremos utilizar el proyecto de otro como el punto de partida del nuestro. Esto se conoce como “fork”.

Clone: Una vez se decide hacer un fork , hasta ese momento sólo existe en GitHub. Para poder trabajar en el proyecto, toca clonar el repositorio elegido al computador personal.

Branch: Es una bifurcación del proyecto que se está realizando para anexar una nueva funcionalidad o corregir un bug.

Master: Rama donde se almacena la última versión estable del proyecto que se está realizando. La rama master es la que está en producción en cada momento (o casi) y debería estar libre de bugs. Así, si esta rama está en producción, sirve como referente para hacer nuevas funcionalidades y/o arreglar bugs de última hora.

Commit: consiste en subir cosas a la versión local del repositorio. De esta manera se puede trabajar en la rama de forma local sin tener que modificar ninguna versión en remoto ni tener que tener la última versión remota, cosa muy útil en grandes desarrollos trabajados por varias personas.

Push: Consiste en enviar todo lo que se ha confirmado con un commit al repositorio remoto. Aquí es donde se une nuestro trabajo con el de los demás.

Checkout: Acción de descargarse una rama del repositorio GIT local (sí, GIT tiene su propio repositorio en local para poder ir haciendo commits) o remoto.

Fetch: Actualiza el repositorio local bajando datos del repositorio remoto al repositorio local sin actualizarlo, es decir, se guarda una copia del repositorio remoto en el local.

Merge: La acción de merge es la continuación natural del fetch. El merge permite unir la copia del repositorio remoto con tu repositorio local, mezclando los diferentes códigos.

Pull: Consiste en la unión del fetch y del merge, esto es, recoge la información del repositorio remoto y luego mezcla el trabajo en local con esta.

Diff: Se utiliza para mostrar los cambios entre dos versiones del mismo archivo.

Bug: Error.

Comandos básicos en la terminal:

pwd: Nos muestra la ruta de carpetas en la que te encuentras ahora mismo.
mkdir: Nos permite crear carpetas (por ejemplo, mkdir Carpeta-Importante).
touch: Nos permite crear archivos (por ejemplo, touch archivo.txt).
rm: Nos permite borrar un archivo o carpeta (por ejemplo, rm archivo.txt). Mucho cuidado con este comando, puedes borrar todo tu disco duro.
cat: Ver el contenido de un archivo (por ejemplo, cat nombre-archivo.txt).
ls: Nos permite cambiar ver los archivos de la carpeta donde estamos ahora mismo. Podemos usar uno o más argumentos para ver más información sobre estos archivos (los argumentos pueden ser -- + el nombre del argumento o - + una sola letra o shortcut por cada argumento).
- ls -a: Mostrar todos los archivos, incluso los ocultos.
- ls -l: Ver todos los archivos como una lista.
cd: Nos permite navegar entre carpetas.
- cd /: Ir a la ruta principal:
- cd o cd ~: Ir a la ruta de tu usuario
- cd carpeta/subcarpeta: Navegar a una ruta dentro de la carpeta donde estamos ahora mismo.
- cd .. (cd + dos puntos): Regresar una carpeta hacia atrás.
(cd + un punto). - Si quieres referirte al directorio en el que te encuentras ahora mismo puedes usar cd . history: Ver los últimos comandos que ejecutamos y un número especial con el que podemos repetir su ejecución.
! + número: Ejecutar algún comando con el número que nos muestra el comando history (por ejemplo, !72).
clear: Para limpiar la terminal. También podemos usar los atajos de teclado Ctrl + L o Command + L.
 TAB: Todos estos comandos tiene una función de autocompletado, o sea, puedes escribir la primera parte y presionar la tecla Tab para que la terminal nos muestre todas las posibles carpetas o comandos que podemos ejecutar. Si presionas la tecla Arriba puedes ver el último comando que ejecutamos.

Recuerda que podemos descubrir todos los argumentos de un comando con el argumento --help (por ejemplo, cat --help).

Conceptos básicos
Directorio: Es la carpeta del proyecto que está en tu disco duro
Staging: Es donde se guardan las modificaciones del archivo antes de enviar la versión final al repositorio (staging es como tener la milanesa empanizada pero no freída).
Repositorio: Es la carpeta donde se guardan las versiones finales de los archivos, todos los que trabajen en el mismo proyecto tienen acceso a esta carpeta y pueden ver qué se ha modificado de un archivo y quién lo realizó.

Estados de un archivo
Untracked: Son todos aquellos archivos que están en el disco duro que no conoce Git.
Staged: Son los archivos que se encuentran en Staging.
Tracked: Son archivos que están en el repositorio o en staging.
Unstaged: Son archivos tracked que han sido modificados, pero no han sido guardados los cambios en staging.

Comandos necesarios
$git mkdir: Crea un directorio.
$git touch: Crea un archivo.
$git init: Define la carpeta del proyecto, crea el staging y el repositorio.
$git add: Guarda la versión del archivo en staging.
$git commit -m””: Guarda el archivo en el repositorio, cada vez que se ejecuta este comando se crea una nueva versión del archivo en el repositorio (en la comillas de -m”” se escribe un comentario sobre las modificaciones para hacer que tus compañeros y tu comprendan posteriormente cuáles fueron los cambios).
$git rm --cached: Cambia el estado de los archivos a untracked.
$git rm --force: Elimina los archivos tanto en el disco duro como en el flujo de Git, aunque queda registro de ese archivo por si se necesita recuperarlo
$checkout: En caso de tener una versión desactualizada de un archivo que está en el repositorio, este comando trae los cambios necesarios al disco duro.

Flujo básico de Git
Con el comando $git mkdir se crea un directorio y los archivos necesarios, los cuales están en estado untracked.
Con el comando $git init se determina el directorio del proyecto, se crea el repositorio y staging.
Con el comando $git touch se crean los archivos necesarios.
4)Conforme se modifican los archivos, se crean versiones de estos con el comando $git add.
5)Al terminar de trabajar en los archivos se guardan en el repositorio con el comando $git commit -m””.

¿Qué es un Branch (rama) y cómo funciona un Merge en Git?
Git es una base de datos muy precisa con todos los cambios y crecimiento que ha tenido nuestro proyecto. Los commits son la única forma de tener un registro de los cambios. Pero las ramas amplifican mucho más el potencial de Git.

Todos los commits se aplican sobre una rama. Por defecto, siempre empezamos en la rama master (pero puedes cambiarle el nombre si no te gusta) y creamos nuevas ramas, a partir de esta, para crear flujos de trabajo independientes.

Crear una nueva rama se trata de copiar un commit (de cualquier rama), pasarlo a otro lado (a otra rama) y continuar el trabajo de una parte específica de nuestro proyecto sin afectar el flujo de trabajo principal (que continúa en la rama master o la rama principal).

Los equipos de desarrollo tienen un estándar: Todo lo que esté en la rama master va a producción, las nuevas features, características y experimentos van en una rama “development” (para unirse a master cuando estén definitivamente listas) y los issues o errores se solucionan en una rama “hotfix” para unirse a master tan pronto como sea posible.

Crear una nueva rama lo conocemos como Checkout. Unir dos ramas lo conocemos como Merge.

Podemos crear todas las ramas y commits que queramos. De hecho, podemos aprovechar el registro de cambios de Git para crear ramas, traer versiones viejas del código, arreglarlas y combinarlas de nuevo para mejorar el proyecto.

Solo ten en cuenta que combinar estas ramas (sí, hacer “merge”) puede generar conflictos. Algunos archivos pueden ser diferentes en ambas ramas. Git es muy inteligente y puede intentar unir estos cambios automáticamente, pero no siempre funciona. En algunos casos, somos nosotros los que debemos resolver estos conflictos “a mano”.

GITFLOW 
1.- Se crea la rama develop, es la rama en la que estamos trabajando (lo que vamos a liberar).
2.- Liberar a producción con tu equipo de trabajo se crea una release desde develop. No se pasa directo de develop a master, Git Flow crea la nueva rama de release.
3.- Por cada petición o tarea se genera una rama llamada feature a partir de develop.
4.- Por ejemplo una pantalla nueva, se crea y está completa el feature de pantalla se cierra y se fusiona con develop.
5.- Cuando tienes la rama release terminada, fusionas con develop y master.
6.- Si hay problema en master se crea hotfix que son los cambios sobre algo que está en producción.
7.- Se crea una nueva rama que trabaja y se reintegra. Una vez que hotfix se completa, se fusiona a ambos develop y master.

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

En la rama master tendremos solo lo que se ha liberado.

https://rogerdudler.github.io/git-guide/index.es.html
https://nvie.com/posts/a-successful-git-branching-model/
https://git-scm.com/book/es/v2
https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
https://danielkummer.github.io/git-flow-cheatsheet/
https://www.youtube.com/watch?v=G_iTZtnlf_U

Volver en el tiempo en nuestro repositorio utilizando reset y checkout
Recuerda que puedes empezar a aprender desarrollo web con el Curso de HTML y CSS.

El comando git checkout + ID del commit nos permite viajar en el tiempo. Podemos volver a cualquier versión anterior de un archivo específico o incluso del proyecto entero. Esta también es la forma de crear ramas y movernos entre ellas.

También hay una forma de hacerlo un poco más “ruda”: usando el comando git reset. En este caso, no solo “volvemos en el tiempo”, sino que borramos los cambios que hicimos después de este commit.

Hay dos formas de usar git reset: con el argumento --hard, borrando toda la información que tengamos en el área de staging (y perdiendo todo para siempre). O, un poco más seguro, con el argumento --soft, que mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.

Al principio es muy difícil entender los conceptos del stage y el commit, lo se. Pero a mi me funciono verlo como una tienda. Les comparto:
Pensemos en una tienda donde comprar un plato de ensalada preparado con tus propias manos. Tu eliges los vegetales y también puedes comprar más de uno.
En el momento que entras a la tienda es tu git init, todo ahí esta pero no todo lo vas a comprar, solo lo tienes a disposición.

Entonces preparas un plato poniendo los vegetales e ingredientes. Haces lo mismo con dos o más platos. Pero solo los que al final vas a comprar los pones en el carrito de compras, ese es tu git add plato_1. Lo que no lo ignoras git ignore plato_2.

Tal vez quieras sacarlos del carrito, eso sería git reset HEAD, pero si queres deshacer un plato que ya elaboraste, como que le quitas todo y pones todos lo vegetales en su lugar de regreso sería git rm --cached

Al final, llevas tu carrito de compras (stage) a la caja para pagar, el cajero te pide un texto o algo para ponerlo en tu recibo de compra, eso seria tu git commit -m “Mi primera compra aquí”. El cajero te da tu numero de recibo (JH6GFD67KJB889JJJNH…)

Así, si quisieras volver a crear un plato en específico que creaste en alguna de tus compras anteriores usas git checkout JH6GFD67KJB889JJJNH… plato_X para volver a tenerlo en tu mano, pero recuerda que tienes que volver a ponerlo en el carrito antes de pasar a la caja. O si pensandolo bien no lo querias, lo regresas con git checkout master plato_x

Con esta analogía, se me ha hecho más fácil ir entendiendo las cosas nuevas que voy aprendiendo de git conforme pasa el tiempo. Solo es cosa de ir encajando todo en su lugar, espero que les sirva a alguno de ustedes también.

GIT RM + GIT RESET
Para volver a commits previos borrando los cambios realizados desde ese commit podemos usar.

git reset --soft [SHA 1]: elimina los cambios hasta el staging area
git reset --mixed [SHA 1]: elimina los cambios hasta el working area
git reset --hard [SHA 1]: regresa hasta el commit del [SHA-1]
Donde el SHA-1 es el identificador del commit

git rm
------------
git rm --cached: Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.
git rm --force: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

git reset
------------
git reset --soft: Borramos todo el historial y los registros de Git pero guardamos los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a un nuevo commit.
git reset --hard: Borra todo. Todo todito, absolutamente todo. Toda la información de los commits y del área de staging se borra del historial.
