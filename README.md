# Decisión de Geolocalización
DECISION DE GEOLOCALIZACION

OBJETIVO:
El objetivo de este proyecto es decidir cual sería la mejor localización para una empresa con ciertas necesidades.  

PASOS:
1.	En primer lugar, hemos visto que los trabajadores de la empresa tenían ciertas necesidades. De esta lista de necesidades hemos decidido escoger todas aquellas que cumplían con el interés general. En primer lugar, queríamos que la empresa estuviese cerca de colegios ya que el 30% de los trabajadores los necesita. Además, hemos decidido estar cerca de sitios de ocio ya que el 100% de la empresa quiere estar cerca de sitios para tomarse algo. También, el 23% de los trabajadores quería estar cerca de Designing companies y otro 23% necesitaba moverse por lo tanto tenían que estar cerca de estaciones. La localización también tenía que estar cerca de startups tecnológicas. Finalmente hemos querido estar cerca de parques para cumplir las necesidades de Dobby y el encargado de mantenimiento. Estando cerca de parques, el encargado de mantenimiento podría jugar al baloncesto y Dobby corretear por ahí.
(Que probablemente lo prefiere a ir a la peluquería).
2.	Para decidir la localización, hemos escogido una localización inicial en San Francisco, Singapur y Londres. 
3.	Llamando a la API Foursquare, hemos podido coger las localizaciones exactas cercanas a nuestra localización inicial filtrando por nuestras necesidades. 
4.	Habiéndonos creado un dataframe con todas nuestras necesidades y con la localización de todos los sitios cercanos a nuestra localización inicial, hemos conectado este dataframe con MongoDB.
5.	Estando todos nuestros datos en MongoDB, utilizando GeoQueries hemos calculado la distancia de cada sitio a nuestra localización inicial.
6.	Para escoger la localización, hemos decidido aplicar un primer criterio de eliminar todas las localizaciones a mas de 1km. Ya que la localización de Singapur no tenía colegios a menos de 1km, esta primera localización ha sido descartada. 
7.	Habiendo calculado todas las distancias de nuestra localización inicial a todos nuestros criterios, hemos multiplicado la distancia por la ponderación que hemos dado a cada lugar.
8.	Ponderaciones: 
Ponderación parques = 0.05
Ponderación Colegios = 0.30
Ponderación StartUps Tecnologicas = 0.05
Ponderación Estudios de Diseño = 0.25
Ponderación Estaciones = 0.2
Ponderación sitios de ocio = 0.15
9.	Teniendo un dataframe con todas las distancias a nuestra localización inicial (máximo 1km) y el valor de cada sitio en base a su ponderación hemos calculado la suma de todos los valores y nos hemos quedado con la localización que tuviese mayor valor. 

La localización con mayor valor ha sido la localización de Londres con una Latitud de Londres Long:-0.0870022262169723, Lat: 51.520624794291884

CONCLUSION
La mejor localización para empezar una empresa entre las tres localizaciones escogidas sería Londres ya que cumple con todos nuestros requisitos y además es el que tiene los requisitos mas cerca. 

LIBRERIAS
 Pymongo,
 Json,
 Pandas,
 Geopandas,
 Dotenv, 
 Os,
 Requests,
 Folium,
 Numpy,
 Pyjsonviewer,
 Shapely. 

