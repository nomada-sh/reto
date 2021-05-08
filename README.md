# Reto: API Rest
Hola, muchas gracias por aceptar el reto, este constá de realizar una API REST en cualquier lenguaje de programación, debes resolver un problema (el cual se redacta mas adelante), debes subir tu proyecto a [github.com](http://github.com) y en tu readme.md redactar las instrucciones de como debemos correr tu API y probarlo.

Se requiere crear una API protegida que reciba un link, posterior a esto, entre al sitio web, extraiga el contenido `HTML` y genere un `CSV` listando todos los enlaces (`<a ...>...</a>`) que encontró. Cuya primera columna será el texto de la etiqueta (`<a>esto</a>`), y segunda columna será el atributo `href` del anchor (`<a href="esto">...`)

## Partes importantes
1 Crear un endpoint `/login` (POST) el cual será un login simulado, el cual va a recibir un email y una contraseña y nos regresara en la respuesta un JWT con el email ingresado en los claims y generado palabra secreta “nomada”.   

El usuario siempre será `demo@usuario.com` y la contraseña: `pipjY7-guknaq-nancex`

🚨 No uses una base de datos, nosotros no vamos a instalar ninguna base de datos por lo cual te pedimos que no la implementes a menos que sea SQLite o algún tipo de persistencia que no requiera instalación extra de algún software para probar tu API en local.

2 Crearás un endpoint `/me` (GET) el cual recibe un header `Authorization: Bearer ...` y me debe responder en JSON los datos guardados en los claims del paso 2   

3 Crear un endpoint `/get-links` (POST) protegido (es decir que se debe mandar un Bearer token o JWT)  el cual recibirá una url, a la cual tu aplicación entrará, extraerá el codigo HTML, y con algún mecanismo creado por ti o por un tercero extraerás todas las etiquetas `<a>` y las listarás en un archivo CSV, este archivo se debe descargar al hacer el llamado a este `endpoint` 

## Requisitos
- [x] Los 3 endpoints deben hacer lo que arriba se redacta.
- [x] Mandarnos el link de tu proyecto en github.com antes de la fecha límite, la cual se te dará via linkedin.
- [x] Documentar como debemos correr tu proyecto, nosotros probablemente nunca hayamos usado el lenguaje que usarás y si no podemos correr tu proyecto quedarás descalificado. (Para nosotros es muy importante que los programadores sepan comunicar ideas y redactarlas)
- [x] Deberás documentar tus 3 endpoints con el formato API Blueprint (https://apiblueprint.org) en un archivo `.apib` que debe estar en la raiz de tu proyecto en el mismo nivel que `readme.md`. (Para nosotros es muy importante que haya una fuente de la verdad para que los programadores front-end tengan como consulta)
- [x] Codigo limpio (https://samuelcasanova.com/2016/09/resumen-clean-code/) un codigo que se pueda leer a la primera es mejor que un codigo elegante o rebuscado.
- [x] Ninguna parte del código debe hacer referencia a Nomada SH

## Puntos extra
- [x] Usar golang
- [x] Generar un XLSX en lugar de un CSV
- [x] Usar una library que interpreta el DOM y con esta poder extraer los `<a>
- [x] Generar pruebas unitarias para tu codigo
- [x] Usar conceptos de clean architecture para segmentar tus carpetas y capas (dominio, aplicación, infraestructura).
  
Mucho éxito, te queremos dentro del equipo.
