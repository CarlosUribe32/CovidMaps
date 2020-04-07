# CovidMaps
Proyecto Final Telemática 2020
# Descripción
Es una aplicación basada en servidores y contenedores la cual ofrecerá información en tiempo real acerca de los casos de la localidad de covid-19 (dependiendo de la localización del usuario) y mediante métodos estadísticos le informará si es seguro salir sin contagiarse o no es seguro 
# ARQUITECTURA
   # README
   Contendrá el informe y la arquitectura del proyecto de la aplicación web
   # principal.html
   Este archivo de hipertexto contendrá la interfaz de entrada que verá el usuario. Aca se obtendran los datos del usuario (incluyendo su      localización actual y si ha tenido covid-19) y se redireccionará al archivo proyect.py
   # proyect.py
   Aca se contendrá el cuerpo del proyecto (se utilizará la libreria flask de python). En este archivo se direccionará las plantillas de      los archivos .html (principal y grafico) y además se regularán los datos que entren por el método POST y se guardarán en una base de        datos del usuario regulada en el servidor mysql
   # grafico.html
   De acuerdo con los datos del usuario enviados por el proyect.py se graficará un mapa el cual mostrará los casos confirmados de Covid-19 
   alrededor de la localización del usuario (solo en Medellín) y se implementará los métodos estadísticos para informarle al usuario si es    seguro salir a la calle o no
   # BaseDatos.db
   Este archivo contendrá la información de los usuarios que accedan a la aplicación web. De acuerdo con esta información se procederá a      realizar el gráfico en el archivo grafico.html y se tendrá de base para graficar nuevos casos de Covid-19 no confirmados en caso de que    el usuario tenga el virus
   # Contenedor en docker
   En el contenedor se almacenarán los archivos ya mencionados en el ubuntu que se usará para el servicio (se tendrá ya instalados el          flask, el pip y la versión de python que se necesitan para soportar el servicio además de la versión apache que se necesita). Así al        momento de levantar una imagen en memoría lo único que se hará es levantar el servicio 
