# CovidMaps
Proyecto Final Telemática 2020
# Descripción
Es una aplicación basada en servidores y contenedores la cual ofrecerá información en tiempo real acerca de los casos locales de covid-19 (dependiendo de la ubicación del usuario en la localidad especificada) y mediante métodos estadísticos le informará si es seguro salir sin contagiarse o no es seguro. Los lenguajes que se usarán para la app web serán python, html y SQL (La interfaz gráfica sera una página web con html)
# ARQUITECTURA
   # README
   Contendrá el informe y la arquitectura del proyecto de la aplicación web
   # Dockerfile
   Este archivo directamente relacionado con el contenedor se encargará de ejecutar las instrucciones necesarias al momento de montar el servidor. Levantara los servicios necesarios y ejecutará el .py por debajo de memoria
   # principal.html
   Este archivo de hipertexto contendrá la interfaz de entrada que verá el usuario. Aca se obtendran los datos del usuario (incluyendo su      localización actual y si ha tenido covid-19) y se redireccionará al archivo proyect.py
   # proyect.py
   Aca se contendrá el cuerpo del proyecto (se utilizará la libreria flask de python). En este archivo de se obtendrán los datos enviados por el principal.html mediante el método POST y a partir de estos se buscará en la Base de datos General la información de los casos de covid-19 de la localidad para realizar el gráfico y el analisis de Riesgo. Si según los datos ingresados el usuario tiene covid-19 o sospecha de ello entonces su información se guardaran en otra base de datos
   # BaseDatosPrincipal.db
   Esta base de datos tendrá la información de los casos confirmados de covid-19 en Medellín
   # BaseDatosSecundaria.db
   Esta base de datos tendrá la información de los casos de covid-19 (o de sospechas) de los usuarios que accedan a la app
   # Contenedor en docker
   En el contenedor se almacenarán los archivos ya mencionados en el ubuntu que se usará para el servicio (se tendrá ya instalados el          flask, el pip y la versión de python que se necesitan para soportar el servicio además de la versión apache que se necesita). Así al        momento de levantar una imagen en memoría lo único que se hará es levantar el servicio 
   # Tipo de servidor y Firewall
   La app web funcionará en un servidor web http (Se usará la libreria flask de python para soportar la app web). Se usuará el UFW como el firewall del sistema habilitando el puerto 80
   
