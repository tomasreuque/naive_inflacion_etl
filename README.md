### naive_inflacion_etl
A raiz de una cuenta de X que remite la inflacion diaria y nos mantiene informados a cerca de ella, me decidi a intentar crear algo similar, un ETL para obtener los precios de los productos en este caso de "www.cotodigital3.com.ar", hacerle alguna modificaion y guardarlo. Para despues hacerlo periodicamente pero con herramientas de cloud AWS


*Vamos a scrapear un codigo que nos permirta tener una vista previa de la pagina web
*Guardar en csv

10/04 actualizacion me estoy amigando con las librerias de request y beautifulsoup4 y logre en primera instancia lo que me propuse, aunque falta mejorar el codigo pera que pueda realizar un scrapping mas exhasutivo

13/04 actualizacion codigo corregido ---> no guardaba la data bien
nuestro codigo usa selenium para obtener de un url de una pagina del tipo eccomerce los productos con su nombre y precio
Mis proximos pasos seran 1) Obtener la totalidad de instacias de una subcategoria
                         2) automatizar el codigo para que recorra todas las categorias y subcatecorias

![Texto alternativo](src/primras.PNG)
necesito iterar sobre las categorias y sub categorias. de momento va a ser hardcodeado


![Texto](src/caaaaaa.PNG)
Como las etiquetas al presionarlas nos dirigen a un link podemos usar el href como parte de el link y eso nos servira para recorrer todas las subcategorias
