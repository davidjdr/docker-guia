# docker-guia
Contenido relacionado a la creación de imágenes y contenedores con Docker para diferentes proyectos

1. Crear una imagen a partir de un archivo Dockerfile en el directorio actual con un tag:

* docker build -t prettyimg:1.0 .

2. Crear un contenedor a partir de la imagen "prettyimg" creada anteriormente

* docker run --rm -it --name prettycontainer -v ~/proyectos/docker-test:/root prettyimg:1.0

* --rm # eliminar el contenedor una vez se ha salido de la terminal
* -it # establece una conexión con la terminal de contenedor al iniciar el mismo en modo interactivo
* -v \~/proyectos/docker-test:/root # monta un volumen de la ruta del host "~/proyectos/docker-test" a la ruta del contenedor "/root"
* prettyimg:1.0 la imagen y tag a ser instanciados por el contenedor


3. Si sólo se desea crear el contenedor se debe ejecutar:

* docker create -it --name prettycontainer -v ~/proyectos/docker-test:/root prettyimg:1.0

* El comando "docker run" crea y ejecuta el contenedor
