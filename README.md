### naive_inflacion_etl
A raiz de una cuenta de X que remite la inflacion diaria y nos mantiene informados a cerca de ella, me decidi a intentar crear algo similar, un ETL para obtener los precios de los productos en este caso de "www.cotodigital3.com.ar", hacerle alguna modificaion y guardarlo. Para despues hacerlo periodicamente pero con herramientas de cloud AWS


*Vamos a scrapear un codigo que nos permirta tener una vista previa de la pagina web
*Guardar en csv

10/04 actualizacion me estoy amigando con las librerias de request y beautifulsoup4 y logre en primera instancia lo que me propuse, aunque falta mejorar el codigo pera que pueda realizar un scrapping mas exhasutivo

13/04 actualizacion codigo corregido ---> no guardaba la data bien
nuestro codigo usa selenium para obtener de un url de una pagina del tipo eccomerce los productos con su nombre y precio
Mis proximos pasos seran 1) Obtener la totalidad de instacias de una subcategoria
                         2) automatizar el codigo para que recorra todas las categorias y subcatecorias

14/04 logre obtener la totalidad de registros para una subcategroria hice un video comentando mis avances pero yt se puso en modo vicera asi que lo recorte y lo estoy subiendo de nuevo



![Texto alternativo](src/segunda.PNG)
necesito iterar sobre las categorias y sub categorias. de momento va a ser hardcodeado

![TTTTTTTT](src/tercera.png)
Le solicite a selenium que me devuelva todas etiquetas de categorias con su respectivas subcategorias, como al presionar la etiqueta de la subcategoria por ejemplo Alfajores, automaticamente nos dirige a la primer pagina que muestra todos los articulos que se han encontrado decidi a partir de eso usar ese valor que es bastante representativo de mi objetivo y tambien tomar la url de la 1er pagina verdad que a futuro me va a servir para realizar las consultas
![Texto](src/caaaaaa.PNG)

Una vez ya haciendo requests de la url de la sub cat me di cuenta que solo me devolvia una determinada cantidad de registros que eran 12, sea cual sea la sub cat me devolvia lo mismo. Despues de intentar sin exito usar la paginacion de la pagina web (mediante el driver para EDGE) para poder recorrer todas las paginas con sus productos. me di cuenta que el url de segunda pagina se comportaba distinto que su contraparte (imagen2). Esta url contenia al final del todo una variable del tipo int sobre la cantidad de resultados que se mostraban en la pagina
![Texxxxx](src/w3wwwwwwww.PNG)

Luego le asigne la variable de cantidad de productos a la variable Nrrp (al url de la segunda pagina), y genere algunas funciones que me permitian a traves de una regex obtener un dataframe con todos los productos de una denominada sub cat en este ejemplo alfajores
![qqqqqqqqqqqqqqqq](src/Captura.PNG)