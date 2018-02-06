# my_repo
GIT Course
Paso 1) Crear un repositorio local vacío de trabajo, llamado my_repo, para realizar el desarrollo que se describe a continuación.

Sugerencia de comandos a utilizar

$ git init (Crea un repositorio git en el directorio actual)

$ git init my_repo (Crea un nuevo directorio llamado my_repo con su repositorio git)

Paso 2) Añadir al directorio de trabajo creado los dos siguientes ficheros.

Un primer fichero llamado README.md con el siguiente contenido:

“Primer fichero en el primer repositorio de <nombre apellidos>”

Un segundo fichero de nombre calculator.html que implemente una calculadora con el botón de x^3 con el siguiente código:

<!DOCTYPE html><html><head>

<title>Calculator</title><meta charset="utf-8">

<script type="text/javascript">

function cube() {

var num = document.getElementById("n1");

num.value = Math.pow(num.value, 3);

}

</script>

</head>

<body>

Number:

<input type="text" id="n1"><p>

<button onclick="cube()"> x^3 </button>

</body>

</html>

 

A este código hay que añadirle debajo de la marca <body>, una línea con el siguiente título HTML:

<h1>Calculadora de ……su nombre y apellidos……</h1>

Sugerencia de comandos a utilizar además del editor:

$ cd mi_repo (Para entrar en el directorio de trabajo)

$ git status (Para conocer el estado de los ficheros)

$ git log --oneline (Para mostrar la historia de commits en formato corto)

Paso 3) Registrar los ficheros en el índice y crear el primer commit en la rama master

 

Sugerencia de comandos a utilizar:

$ git add <fichero1> <fichero2> …

$ git commit -m “x^3 button”

Paso 4) Modificar el fichero calculator.html para añadir un segundo botón a la calculadora que eleve un número a la cuarta potencia (x^4) y cerrar un segundo commit en la rama master.

Sugerencia de comandos a utilizar:

    $ git status -s (muestra el estado de los ficheros)
    $ git log --oneline (muestra la historia de commits en formato corto)
    $ git diff …. (muestra las diferencias con el commit anterior antes y después de cerrarlo)
    $ git add . (registra todos los ficheros nuevos o modificados en el índice)
    $ git commit -m “x^4 button” (cierra el commit, añadiéndole el mensaje indicado)
     

Paso 5) Crear una rama de nombre sine que comience en el primer commit (con mensaje “x^3 button”) y restaurarla en el directorio de trabajo.

Sugerencia de comandos a utilizar:

$ git branch -v (muestra las ramas existentes en el repositorio)

$ git checkout -b sine <id_de_commit> (Crea rama en commit indicado y realiza checkout a rama).

Paso 6) Modificar en la rama sine el fichero calculator.html del directorio de trabajo añadiendo un segundo botón al commit de la calculadora que solo tiene el botón x^3. El nuevo botón debe calcular el seno de un número (sin(x)).

Una vez añadido el nuevo botón a la calculadora de la rama sine, registrar el fichero modificado calculator.html en el índice y crear un nuevo commit en la rama sine.

Sugerencia de comandos a utilizar:

    $ git branch -v (muestra las ramas existentes en el repositorio)
    $ git status -s (muestra el estado de los ficheros)
    $ git log --oneline (muestra la historia de commits)
    $ git diff ….. (muestra las diferencias con el commit anterior antes y después de cerrarlo)
    $ git add . (registra todos los ficheros nuevos o modificados en el índice)
    $ git commit -m “sin(x) button” (cierra el commit, añadiéndole el mensaje indicado)
    $ git log --oneline --all (Para mostrar la historia de todas las ramas en formato corto)

 

Paso 7) Integrar la rama master en la rama sine con el comando git merge master. La integración tiene conflictos, que se deben resolver con el editor. Una vez resueltos, debe finalizar la integración (merge) creando el commit de integración con git commit …

Sugerencia de comandos de git a utilizar:

    $ git merge master (ejecutar este comando estando en la rama sine)
    $ git status -s (para ver los ficheros con conflictos despees de integrar las ramas)
    $ git diff xxx (para ver diferencias en el fichero xxx)
    $ git add . (para registrar ficheros modificados en el índice)
    $ git commit -m “integrate master” (para finalizar la integración cerrando el commit)
    $ git log --oneline --graph (Para mostrar la historia de integraciones de la rama)

 

Paso 8) Integrar el commit de integración de la rama sine en la rama master con el comando git merge master. Como el grafo de commits indica que la integración se ha realizado ya en la rama sine, git realiza la integración con Fast-Forward, reutilizando el commit ya generado en la integración del punto anterior y simplemente avanza el puntero de rama a dicho commit.

Sugerencia de comandos de git a utilizar:

$ git merge sine (ejecutar este comando estando en la rama master)

$ git log --oneline --graph --all (Para mostrar la historia de integraciones de todas las ramas)

Paso 9) Crear una cuenta en GitHub que incluya su nombre y apellidos (o sus iniciales) en el nombre de la cuenta. Si ya tiene una cuenta con estos requisitos puede utilizarla.

Paso 10) Crear en la cuenta de GitHub anterior un repositorio vacío de nombre my_repo.

Paso 11) Subir todas las ramas del repositorio local al nuevo repositorio en GitHub.

Sugerencia de comandos a utilizar:

$ git push --all https://github.com/<su_cuenta>/my_repo
