# Prueba Técnica Ulfix | Conexión a API

## Introducción
Para esta prueba será necesario generar un chart utilizando las siguientes herramientas:

API | Coindesk [CoinDesk](http://www.coindesk.com/) Para este ejercicio deberás conectarte a la API de Coindesk con los datos de Bitcoin [Bitcoin Price Index](https://web.archive.org/web/20191106152143/https://www.coindesk.com/api). Requeriremos que realices la representación de dichos datos de manera programática.

Representación gráfica | Chart.js [Chart.js](http://www.chartjs.org/) Para este ejercicio deberás representar el gráfico ya sea en un Canvas de HTML o en una vista de Handlebars

## Requerimientos
  
  - Forkear este repositorio
  - Clonarlo en una ubicación local de este equipo (será necesario que tengas una cuenta de gitHub para evaluar tu manejo de control de versiones, en caso de no tenerla, puedes abrirla y hacer tu repositorio público)
  
## Comandos Git

Una vez creado el repositorio correr los siguientes comandos
```
$ git add .
$ git commit -m "done"
$ git push origin master
```
Y crear un pull request para poder revisarlo

# Instrucciones

En el starter code podrás encontrar una estructura en Express para iniciar el proyecto sin pérdida de tiempo, asímismo, existe un archivo en JavaScript para que agregues tu codificación de Ajax

```
starter-code/
├── .gitignore
├── app.js
├── bin
│   └── www
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   │   └── financial-data.js
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
└── views
    ├── error.hbs
    └── index.hbs
```
Al final, deberás representar algo parecido a lo siguiente

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_b94d2137d3737b49ecf92ee8709f5a14.png)

## Primer iteración: Obtener data del API

Primero deberás obtener la data de la API para ser representada en el chart. Para ello utilizaremos la siguiente API [CoinDesk API Documentation](https://web.archive.org/web/20191106152143/https://www.coindesk.com/api)

Tendrás que hacer una presentación del histórico de datos en el chart haciendo una petición `GET` hacia la siguiente URL `http://api.coindesk.com/v1/bpi/historical/close.json` (puedes utilizar testing en Postman). El response deberá ser un objeto json.

Deberás realizar un AJAX request por lo tanto es necesario que importes el CDN de Axios.
TIP: Para probar tu request a la URL utiliza un `console.log()` para estar seguro de la petición.

## Segunda iteración: Crear el chart

Una vez que la petición sea exitosa, deberás mostrar el chart en la vista (Canvas o Handlebars). Usaremos [Chart.js](http://www.chartjs.org/) por lo que será necesario que agregues el CDN.
Una vez agregada la referencia CDN al HTML deberás representar la información obtenida en el json del paso 1 en un [Line Chart](http://www.chartjs.org/docs/#line-chart-introduction)



