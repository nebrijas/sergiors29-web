# AD3

Nos encontramos en la actividad dirigida 3, la cual consiste en realizar un ejercicio de programación literaria aprovechando el código con Python utilizado en clase de Programación para realizar _web scraping_.

A continuación coloco el código fuente:

### Código Fuente


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
 
resultados = []
 
req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')
 
tags = soup.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')
 
tags = soup2.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')
 
tags = soup3.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')
 
tags = soup4.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')
 
tags = soup5.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')
 
tags = soup6.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')
 
tags = soup7.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')
 
tags = soup8.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')
 
tags = soup9.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')
 
tags = soup10.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')
 
tags = soup11.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')
 
tags = soup12.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')
 
tags = soup13.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')
 
tags = soup14.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')
 
tags = soup15.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')
 
tags = soup16.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')
 
tags = soup17.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
 
os.system("clear")
 
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
 
print(colored("Igualdad", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))
 
print(colored("Mujeres", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))
 
print(colored("Mujer", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))
 
print(colored("Brecha salarial", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))
 
print(colored("Machismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))
 
print(colored("Violencia", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))
 
print(colored("Maltrato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))
 
print(colored("Homicidio", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))
 
print(colored("Género", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))
 
print(colored("Asesinato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))
 
print(colored("Sexo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

    La llegada de Petro abre una nueva era en las relaciones entre Caracas y Bogotá
    Latinoamérica muestra su músculo ante el inicio del alza en las tasas de interés
    La salida dialogada a la crisis de Ecuador se estanca en el pulso indígena al Gobierno
    Asfixia indígena en Ecuador
    Cuidado: aquí hay historia
    ¿Tendrá la inseguridad un costo político para López Obrador?
    Ucrania y lo que significa para la ampliación de la UE
    Las incógnitas de la pastilla milagrosa contra un tipo de calvicie
    Un incendio en el centro de Buenos Aires causa cinco muertos y varios heridos
    Marilynn Malerba, la jefa de la tribu india Mohegan que firmará los nuevos billetes en Estados Unidos
    Núria Vilanova: “España es el segundo inversor en América Latina pero no puede bajar la guardia”
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    El neurólogo que descubrió 11 enfermedades: “El cerebro es aún un enigma”
    Carlos González, pediatra: “No hacer caso a un niño que llora, tenga la edad que tenga, me parece una solemne tontería” 
    Susto en el Mundial de natación: rescatada una nadadora que se desmayó en el agua
    ¿Se puede dejar de roncar?
    En la biblioteca de Mario Vargas Llosa: “Nunca me he sentido extranjero gracias a los libros”
    La carrera de obstáculos de Ucrania para entrar en la UE
    Alemania activa la segunda fase de su plan de emergencia tras los recortes de gas de Rusia
    Vicente Fox: “Sigo en política porque a México se lo está llevando el carajo”
    “Yo no tuve infancia”: la huida de Catalina de todas las violencias de su vida con solo 16 años
    El Reino Unido detecta el virus de la polio en las aguas de Londres
    Congo recupera de Bélgica lo único que queda de su héroe nacional, Patrice Lumumba: un diente
    Diego Luna: “Nadie nos enseña a decir adiós”
    Un viaje en el tiempo con Kurt Vonnegut
    El arte nos repara emocionalmente
    La arquitecta Margarita Jover: “Me resisto a que el capital decida la forma del mundo”
    El legado de cuatro siglos de colonialismo, racismo y esclavitud de Países Bajos se expone en Ámsterdam
    Brad Pitt cree que está llegando el final de su carrera: “Me veo ya en mi última etapa”
    Los gestos de Charlene y Alberto de Mónaco para zanjar los rumores de crisis
    Adam Sandler: de despreciado por la crítica a apuesta de Oscar
    
    El chef que sirve compost y corteza de árbol quemado
    Ellos no bailaron solos: la mujer detrás de la loca historia de Locomía
    This is for la Raza: 50 años de arte chicano
    Pasar por Estados Unidos: ¿una obligación para el desarrollo artístico?
    Gustavo Petro: la victoria final
    Ciudad Oculta: las drogas y el hambre no ceden en Argentina
    Bruno Pereira, un funcionario convertido en activista para proteger a los indígenas
    Así era América antes de que Colón la descubriera
    Belgium gives back to Congo the only thing left of its national hero, Patrice Lumumba: A tooth
    Jeffrey Sachs: ‘Something is wrong with the American system. And in human nature’
    Yves Coppens, one of the discoverers of famous fossil ‘Lucy,’ dies at 87
    Wes Craven, the master of horror who wanted to direct dramas
    Shaquille O’Neal, the king of franchises: 155 burger joints, 40 gyms and a fortune of $400 million
    How Beyoncé resurrected house music
    Letras Americanas: la actualidad literaria de un continente vista por el escritor Emiliano Monge
    Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
    Toda la actualidad científica en el boletín de Materia
    Ideas: reportajes y entrevistas para entender el mundo
    La comisión del 6 de enero se centra en las presiones y amenazas de Trump a varios funcionarios  para que no certificaran el triunfo de Biden
    Texas tilda de “fracaso despreciable” la respuesta de la policía ante el tirador de Uvalde 
    El día en que Petro ganó a Petro
    Latinoamérica muestra su músculo ante el inicio del alza en las tasas de interés
    La inflación en México vuelve a escalar y se sitúa en 7,88% en junio
    Marilynn Malerba, la jefa de la tribu india Mohegan que firmará los nuevos billetes en Estados Unidos
    Por qué estamos cada vez más deprimidos
    La expansión de la viruela del mono empuja a la OMS a decidir si es una emergencia internacional
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    Así suena ‘Break My Soul’, lo nuevo de Beyoncé 
    Michael J. Fox, Diane Warren, Peter Weir y Euzhan Palcy recibirán los Oscar honoríficos
    María Pagés: “A los lugares cercanos se va a seguir yendo, pero a los lejanos… quién va a poder comprar los billetes”
    El neurólogo que descubrió 11 enfermedades: “El cerebro es aún un enigma”
    La metástasis del cáncer avanza durante el sueño
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    El trampolín de Mallorca hacia Wimbledon
    Nadal reverdece en Hurlingham
    Laporta pide militancia en el Camp Nou tras la invasión de 30.000 seguidores del Eintracht 
    Vivir frente a un “vertedero” en el centro de Madrid: estruendo, hedor y ratas en Tirso de Molina
    Sierra de la Culebra: un incendio gigantesco que no pone en peligro a los lobos, pero sí un modelo de convivencia ejemplar
    La construcción de 52 viviendas en una playa de Begur desata la indignación de las redes
    ¿Sigue siendo imprescindible tener un antivirus? 
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    ‘En esta crisis energética se mató la transformación digital’, por Paloma Llaneza
    El exministro Jorge Fernández Díaz dirigió la Operación Cataluña contra Pujol
    La mayor asociación policial intenta burlar la seguridad de la cumbre OTAN con mini protestas 
    Cae una red que traficaba con armas de guerra y las vendía a delincuentes
    ‘Supervivientes’ y la incultura general
    Un viaje en el tiempo con Kurt Vonnegut
    ‘Intimidad’ o la denuncia de un delito del siglo XXI 
    Los problemas crecen para los Bieber: Hailey, demandada por la marca de cosmética que lanzó hace una semana
    Guillermo de Inglaterra cumple 40 años como el candidato ideal para seguir la estela de Isabel II
    Los 40 años de Guillermo de Inglaterra en 16 fotos
    La discriminación contra las minorías sexuales limita el desarrollo de Latinoamérica
    ¿Cómo se curan los sistemas de salud luego de una pandemia?
    Así fue nuestra experiencia de escribirnos con GPT-3, una máquina de inteligencia artificial
    Viaje al fin de Occidente, en la gran frontera entre Finlandia y Rusia
    Guy Standing: “Hemos dejado que la derecha se apropie de la libertad”
    Así era América antes de que Colón la descubriera
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    En los sesenta, todo se vendía con fotos
    De cómo Beyoncé resucitó la música ‘house’
    La culpa de todo la tiene el modelo de desarrollo
    El precio del combustible colma la paciencia de los sudafricanos
    24 horas en San Vicente de la Barquera, la villa donde canta el mar
    Las reseñas de los turistas, tan útiles o tan inútiles: una cuenta de Twitter señala comentarios absurdos sobre Asturias
    Brooke Shields: «Fue duro querer a mi madre alcohólica porque me sentía responsable de ella»
    Aura García-Junco, sobre las relaciones abiertas: “Quería entender por qué generan tanto rechazo”
    Eugenia Silva: “No he vivido situaciones extremas. Sabía qué quería y hasta dónde llegar”
    Las frustraciones de Wes Craven, el genio del terror que quería dirigir melodramas
    Ensalada de pollo, nísperos y queso feta
    Latkes: las irresistibles tortitas fritas de patata
    Amazon expande su plantilla en España y contratará 2.000 trabajadores en 2022
    “Estaban paralizados y me he tirado”: Andrea Fuentes relata su rescate a una nadadora que se desmayó
    Ponte a prueba con nuestros crucigramas, sopas de letras, sudokus y juegos arcade
    Errejón dispara los comentarios con lo que ha hecho tras ese tuit de Lucía Etxebarria
    Zidane, sobre entrenar al PSG: “Nunca digas nunca”
    ¿Y si Internet se cae? Pánico al apocalipsis digital
    Alemania activa la segunda fase de su plan de emergencia ante la escasez de gas tras los recortes de suministro de Rusia 
    La candidatura de Ucrania espolea la impaciencia de los Balcanes para ingresar en la UE 
    Vídeo | Rusia vuelve a mirar a Járkov: análisis de la ofensiva de Putin en el este de Ucrania
    Exiliados rusos
    Cambio en Colombia
    Las elecciones reparlamentarizan Francia
    Emmanuel Macron pierde las legislativas en Francia 
    ¿La democracia es una sola mujer trabajadora en la Asamblea de Francia?
    Reformas en justicia, corrupción y oligarcas: la carrera de obstáculos que Ucrania debe recorrer para entrar en la UE 
    El ministro de Infraestructuras de Portugal: “Es imperdonable que portugueses y españoles no resolvamos las conexiones ferroviarias”
    Congo recupera de Bélgica lo único que queda de su héroe nacional, Patrice Lumumba: un diente
    Los talibanes, aislados y sin recursos, piden ayuda internacional para la emergencia del terremoto en Afganistán
    Más de un millar de muertos en el sudeste de Afganistán por un terremoto de magnitud 6,1
    El bloqueo lituano al enclave de Kaliningrado abre un nuevo frente de guerra entre Rusia y la UE 
    Hallados los cadáveres de los dos sacerdotes jesuitas y el guía turístico asesinados en la sierra Tarahumara
    Gustavo Petro comunica al Gobierno venezolano su intención de reabrir la frontera 
    La salida dialogada a las protestas de Ecuador se estanca en el pulso indígena al Gobierno
    Cuatro trenes y 11 horas: Lisboa y Madrid peor conectadas que en 1881 
    El Gobierno de Bulgaria cae tras solo seis meses en el poder al perder una moción de censura
    Demócratas y republicanos alcanzan el primer acuerdo en décadas para el control de armas en Estados Unidos
    La Corte Suprema argentina deja libre el camino para juzgar a Cristina Kirchner en una causa por corrupción
    La comisión del 6 de enero se centra en las presiones y amenazas de Trump a varios funcionarios  para que no certificaran el triunfo de Biden
    Ecuador advierte de que “la democracia está en serio riesgo” por las protestas indígenas
    Las protestas en Ecuador, en imágenes
    El clima incendiado
    Asfixia indígena en Ecuador
    Ucrania y lo que significa para la ampliación de la Unión Europea
    Cuidado: aquí hay historia
    Vidas gitanas
    Una nueva Colombia le habla al mundo
    Un Gobierno en la desesperación
    Hermana Mónica, yo sí te creo
    País de puritanos, cotillas y empáticos 
    La viruela del mono, sin estigmas
    La búsqueda de seguridad vence al cabreo
    Concesiones territoriales
    Yo vi el vídeo 
    El Roto
    Peridis
    Flavita Banana
    Riki Blanco
    Sciammarella
    Planeta de Plástico, por Malagón
    Envía tu carta
    La proyección de las elecciones en Andalucía
    Siempre pierden los mismos: los agricultores
    ¿Aún hay guerra?
    Opinar sin insultar
    Contra el conflicto de intereses, transparencia
    Entre los derechos de Esther López y los de los lectores
    El defensor del lector contesta
    El Gobierno negocia un cheque para cuatro millones de beneficiarios vulnerables ante el golpe de la inflación
    El Ejecutivo lleva aprobados más de 10.000 millones en medidas en lo que va de año
    Así giró Andalucía: la derecha lleva años creciendo sobre todo en barrios pobres
    La búsqueda de seguridad vence al cabreo
    Los errores se pagan
    Desborde popular en Andalucía
    Demasiado ruido en el Gobierno de coalición
    La ‘confederalización’ del PP
    Anticorrupción archiva la investigación sobre la compra de mascarillas de la Comunidad de Madrid de la que se benefició el hermano de Díaz Ayuso 
    Biden se reunirá con Sánchez y con el Rey en su viaje a Madrid para la cumbre de la OTAN
    Muere Teodulfo Lagunero, militante del PCE que introdujo a Carrillo en España de forma clandestina
    Fernández Díaz dijo al juez que nunca despachó con Villarejo: “No he tenido ni una sola relación con él”
    La mayor asociación policial intenta burlar la seguridad de la cumbre OTAN con mini protestas 
    Ayuso, al borde de las lágrimas tras el archivo del caso de las mascarillas: “Aquí no hay corrupción”
    El exministro Jorge Fernández Díaz dirigió la Operación Cataluña contra Pujol
    El PSOE pide a Feijóo, tras la publicación de los audios de Fernández Díaz, que asuma su responsabilidad de “prácticas mafiosas” 
    Detenido Paul Wouter, el exmilitar brasileño que fingió su muerte al caer en una redada con narcos gallegos
    El ruido se apaga en el Congreso tras las elecciones andaluzas
    Sánchez anuncia una nueva rebaja del IVA de la luz, que pasará del 10% al 5%
    Un paraíso en el que avistar más de 20 especies de cetáceos
    El secreto de Fuerteventura se hace viral: la ‘playa de las palomitas’
    Artesanía y cultura que conquista a las ‘influencers’
    Más allá de la capital. El triunfo de la vida rural madrileña
    Así lucha la tierra del cerezo para conseguir un nuevo florecimiento económico
    “Siempre me ha parecido que los que iban disfrazados eran los demás”
    “La herramienta más poderosa para salvar a la humanidad son las matemáticas”
    El Gobierno y sus socios aprobarán la semana que viene el recargo al sector fósil para rebajar la factura de la luz
    La Audiencia Nacional archiva la causa contra Sánchez Galán por los encargos de Iberdrola a Villarejo
    Abengoa agota los plazos para el rescate y alarga su calvario
    El ansiado “tren rápido” de Extremadura comienza a circular por la región más de dos décadas después de su anuncio
    Invierno crudo
    Aterrizaje suave sin fragmentación
    Las finanzas que corroen la industria 
    El ajuste fiscal que viene: ¿Qué opinan los ciudadanos?
    Una oportunidad perdida en el proceso de las energías renovables 
    Indra cesa a cinco consejeros independientes con el apoyo de la SEPI, SAPA y Amber
    El nuevo túnel entre Chamartín y Atocha se abrirá el 1 de julio, pero sin efectos prácticos para el viajero del AVE
    José Manuel Entrecanales: “Estamos ante una catástrofe medioambiental sin precedentes”
    Tendam (Cortefiel) vuelve a los beneficios en 2021 tras disparar las ventas un 43%
    Marilynn Malerba, la jefa de la tribu india Mohegan que firmará los nuevos billetes en Estados Unidos
    Cegos toma aire tras la entrada de Bridgepoint
    Ford elige la factoría de Almussafes para fabricar sus nuevos coches eléctricos y garantiza su continuidad
    La industria alimentaria advierte del peligro de desabastecimiento general si hay otra huelga de transportistas
    Así fue la negociación final que desatascó la huelga del metal de Cantabria
    Sánchez anuncia una nueva rebaja del IVA de la luz, que pasará del 10% al 5%
    Rosauro Varo, presidente de GAT Inversiones y Jorge Gallardo, presidente de Vithas, Premio Emprendedor del Año de EY
    Ferrari corre hacia un mundo más verde y caro
    Vientres de alquiler: una boyante y turbia industria que aprovecha las rendijas legales para enriquecerse
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    Así es la española que revoluciona las burbujas de champán más exclusivas
    El TSJ de Madrid decidirá sobre la legalidad de la Operación Chamartín tras recibir nueve recursos
    
    El Corte Inglés avanza hacia un capital estable y español con la salida a Bolsa de fondo
    Héctor Grisi, a la plantilla de Santander: “Tenemos que ir más rápido”
    Valencia será el centro de la electromovilidad española con las baterías de VW y los coches de Ford
    Líos en la piscina comunitaria: normas y sentencias para un chapuzón seguro
    Parir en casa, educarlo por mi cuenta… ¿Qué puedo decidir sobre mi hijo y qué no?
    Saltarse un paso a nivel de camino a la oficina es accidente laboral
    ¿Es esta la edad dorada del emprendimiento universitario?
    Y después de la EBAU, ¿qué?
    Joan Ramón Castelló: “En la formación ‘online’ hay que ser realistas con el tiempo disponible y contar con el apoyo de la familia”
    Cancerberos del bienestar de la empresa
    Salud a golpe de clic con la cercanía del médico de cabecera
    Cómo garantizar la seguridad en un mundo de amenazas híbridas
    ¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
    Las aventuras de un par de calcetines que dan empleo a todo un pueblo
    Cultura financiera como punto de partida para volver a empezar
    Por qué digitalizar una pyme aporta más empleo
    Logística a bajas temperaturas, la revolución que vino del frío
    ‘Coopetir’: la actitud DFactory
    Así serán las ciudades de la (nueva) última milla
    PERTE Agroalimentario: ¿cómo acceder a los fondos europeos?
    Claves para internacionalizar mi negocio
    ¿Crisis de deuda mundial a la vista?
    ¿Está al frente España de la revolución del hidrógeno? 
    El momento de la energía solar
    Las principales reformas (con subvención europea) para ahorrar energía en la vivienda
    Gloria Ramos, cuando el afán de superación acaba en la alfombra roja 
    La importancia de la cultura financiera para tener una buena jubilación
    Hotmart y su plataforma 360 para creadores de contenidos
    Una aplicación para presentar la declaración desde casa y conseguir los máximos beneficios
    La Iglesia insiste en que no abrirá sus archivos al Defensor, aunque cederá datos de casos concretos que le solicite
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    Un año de eutanasia en España: 172 casos y una gran desigualdad entre las comunidades autónomas
    Una mañana de luz blanca: relato de un médico tras su primera eutanasia
    La lucha contra la ELA: el 8 de marzo nació un colectivo esperanzado
    La pederastia, problema de poder
    Educación y trabajo: ¿cómo lograr este binomio perfecto en Iberoamérica?
    La expansión de la viruela del mono empuja a la OMS a decidir si es una emergencia internacional
    El conde de Atarés asesinó a su mujer el día en que se disponía a abandonarle
    Sanidad descarta que la infección de la finca de Toledo sea un caso de cólera, aunque esté causada por la misma bacteria
    Las autoridades sanitarias del Reino Unido detectan el virus de la polio en las aguas residuales de Londres
    Seis de cada diez ciudadanos viven en comunidades autónomas con servicios sociales debilitados
    La policía detiene a la expareja de una mujer cuyo cadáver fue hallado en el Guadalquivir
    Consumo creará un organismo para inspeccionar y sancionar fraudes masivos en España
    Armas, nobleza y violencia machista: ¿hay menor percepción de gravedad en las clases socioeconómicas más altas?
    Sierra de la Culebra: un incendio gigantesco que no pone en peligro a los lobos, pero sí un modelo de convivencia ejemplar
    Las farmacias podrán dispensar compuestos del cannabis dentro de seis meses 
    Estados Unidos planea reducir la cantidad de nicotina de los cigarrillos para que no sean adictivos
    Mitos, falsedades, bulos y realidades sobre el VIH 40 años después
    Educadores con VIH para minimizar el impacto tras el primer diagnóstico
    El tremendo peso de la obesidad en España
    Interactivo | Los 14 cambios en los aeropuertos españoles que no ves y que ya están ocurriendo
    Encontrar empleo pese a los obstáculos. Por dónde empezar la búsqueda
    La fórmula de Carboneros para evitar el éxodo rural: trabajar cuidando a los vecinos 
    Consejos y cuidados para el primer verano con un gatito o un perrito
    ¿Qué tienen en común perros y gatos cuando son cachorros?
    La guía definitiva para alimentarnos mejor (y cuidar nuestra salud y la del planeta)
    Más vida después del cáncer de próstata avanzado 
    Cáncer de ovario, el más rebelde de los tumores ginecológicos
    El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
    La salud mental de los refugiados: cómo abrirse para cerrar las heridas
    El desconocido (y esencial) apoyo de los farmacéuticos a los pacientes crónicos
    El esfuerzo de una paciente por convertirse en su doctora
    Así es la vida de los refugiados ucranianos en España
    ¿Cómo será el envase para alimentos y bebidas del futuro?
    Un aula de Vallecas se rebela contra los libros de texto que silencian a las mujeres
    Solo un 3% de alumnos de Cataluña pidió hacer el examen de Selectividad en castellano
    Subirats reinterpreta la ley de Universidades: freno a la precariedad, facilidades para los alumnos extranjeros y ciencia abierta
    “Los profesores no van a cambiar de golpe su forma de trabajar el curso que viene por la nueva ley educativa”
    Trampantojo de pescado y lasaña vegetal en el comedor: cientos de colegios buscan fórmulas para que llevar la alimentación responsable a los niños
    Vídeo | Las recetas del cocinero escolar para que los niños de El Grau coman sano y rico 
    Así puede convertirse un colegio en un espacio más fresco sin usar aire acondicionado
    209.691 candidatos compiten por una plaza en la última convocatoria sin ventaja aplastante para los interinos
    El mileurismo asoma en la mitificada carrera de dentista: “Nunca imaginé una situación así”
    Las notas de la Selectividad 2022: del 93% de aprobados en Canarias y el 94,5% en Madrid, al éxito casi total en La Rioja
    Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
    Sin currículos
    La escuela concertada ante las desigualdades: el debate pendiente
    La equidad frente a las políticas educativas de privatización en Andalucía
    No hay lunes al sol en la Universidad
    Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
    Una fórmula para que la escuela pública compita mejor con la concertada
    La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
    El Ayuntamiento de Madrid guarda en un cajón una herramienta ya pagada para ver los datos de contaminación al detalle 
    La implantación del nuevo Bachillerato general fracasa pese a su demanda potencial: “Creímos que lo pedirían seis alumnos y lo han hecho 27”
    Toni Solano, director de instituto: “Veo mal a los niños, necesitan muchísima ayuda”
    Niños, Administraciones y redes sociales: prohibir su uso con una mano y enseñar a crear contenidos con la otra
    El Gobierno aprueba el decreto de bachillerato: los alumnos podrán terminar con un suspenso y desembocará en una nueva Selectividad
    La ley del silencio dentro y fuera del aula
    Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
    Golpe a la temporalidad en las universidades: 25.000 profesores asociados serán indefinidos a tiempo parcial
    Antonio Abril: “Yo le decía a Castells: ‘Tienes que aguantar la presión, tienes que hacer la reforma universitaria”
    Los universitarios extranjeros podrán quedarse un año en España automáticamente al terminar la carrera
    Sierra de la Culebra: un incendio gigantesco que no pone en peligro a los lobos, pero sí un modelo de convivencia ejemplar
    La indignación crece sobre las ascuas del incendio en la sierra de la Culebra
    Jardines en los tejados, árboles africanos y calles pintadas de blanco: cómo adaptar la ciudad al calor extremo
    La construcción de 52 viviendas en una playa de Begur desata la indignación de las redes
    Un continente mortal para los defensores de la tierra
    Drama en la sierra de la Culebra, el paraíso del lobo ibérico que quedó abrasado por un rayo
    Alemania anuncia que recurrirá al carbón ante el recorte de suministro de gas ruso
    La inacción frente al cambio climático hará que sea habitual superar los 40 grados en junio en España
    Ibrahim Thiaw: “Hay que prepararse mejor frente a las sequías, los agricultores franceses están cultivando ya cereales africanos”
    La ola de calor provoca la caída de cientos de crías de vencejo en las calles de Sevilla y Córdoba
    “En Singapur ya se vende carne cultivada para alimentación” 
    La lección del martín pescador para afrontar la crisis ecológica
    Estocolmo+50: mirar atrás para tomar impulso
    El verano ya no es lo que era 
    Juan Serna, Premio Nacional de Medio Ambiente: un reconocimiento merecido
    Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
    La UE abraza las renovables para romper la dependencia de Rusia
    La lucha en un pueblo de Teruel para salvar su última montaña
    ¿Qué aire respiran los niños de Madrid y Barcelona? En el 46% de los colegios se supera la contaminación permitida
    El Congreso aprueba la reforma de la ley de la ciencia sin votos en contra
    Las incógnitas de la pastilla milagrosa contra un tipo de calvicie
    ¿Se puede dejar de roncar?
    El síndrome del hombre lobo y la realidad lógica de su fábula
    Muere Yves Coppens, uno de los descubridores del fósil más famoso del mundo 
    Ni patentes, ni firmar estudios: las científicas reciben mucho menos reconocimiento por su trabajo
    La metástasis del cáncer avanza durante el sueño
    A la caza de exolunas, la próxima frontera de exploración planetaria
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer 
    Eloísa del Pino sustituye a Rosa Menéndez al frente del CSIC
    Los restos de un cohete chino, visibles desde varios puntos de España al atravesar el cielo
    Los humanos, más próximos a la tolerancia de los bonobos que a la belicosidad de los chimpancés
    Escarabajos peloteros: insectos dialogando con el firmamento
    Una piedra hallada en Egipto en 1996 podría ser la primera evidencia en la Tierra de una supernova insólita
    La costa de los gigantes: huellas en el golfo de Cádiz confirman la coexistencia de uros enormes con otra megafauna y neandertales 
    A la caza de exolunas, la próxima frontera de exploración planetaria
    Reaparece la tesis de María Wonenburger, la pionera matemática española que permaneció décadas en el olvido
    Técnicas criptográficas que se fundamentan en lo impredecible
    Las matemáticas de los juegos malabares
    Matemáticas para apilar naranjas
    Números McNugget
    La moneda de Frobenius
    D’Alembert y el cálculo de probabilidades
    El síndrome del hombre lobo y la realidad lógica de su fábula
    La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
    El andar del borracho, las huellas del azar y el juego de dados en algunos libros malditos
    El campo vibratorio y las fronteras de la ciencia desde un punto de vista científico
    Paul Auster fluctuando entre el pudin de pasas y la nube de mosquitos
    ¿Son mejores las hormonas bioidénticas?
    ¿Qué surgió antes, el ARN o el ADN?
    ¿Por qué se sabe que los núcleos de la Tierra rotan?
    ¿Qué son los mini reactores nucleares?
    Invitados indeseables por Navidad: el muérdago y otras plagas que evitar durante las fiestas
    Las ‘apps’ nutricionales o cómo comer bien no debería depender de uno mismo
    Malnutrición invisible: el impacto de la pobreza en la salud infantil
    El óxido de etileno, la sustancia cancerígena que ha obligado a retirar miles de alimentos en la UE
    Que no te líen con los ingredientes: aceites y grasas de mala calidad nutricional
    ¿Es el Torico de Teruel una falsificación? La restauración tras una caída desata la sospecha de que sea una copia de la Guerra Civil
    La arquitecta Margarita Jover: “Me resisto a que el capital decida la forma del mundo”
    La pintora Carmen Álvarez-Coto acaba con el misterio y vuelve después de tres décadas de retiro voluntario
    El libro que explica qué significa ‘votar normal’
    El poeta
    Ese país salvaje llamado España
    Mercedes, mira por nosotros
    La Unesco alerta sobre los ataques a más de 150 espacios culturales en Ucrania
    El legado de cuatro siglos de colonialismo, racismo y esclavitud de Países Bajos se expone en Ámsterdam
    Diego Luna: “Nadie nos enseña a decir adiós”
    Manuel Jabois: “Ni por 100 millones dejaría de escribir”
    Vídeo | En la biblioteca de Mario Vargas Llosa: “Nunca me he sentido un extranjero gracias a los libros”
    El concierto más emocionante de Pablo Milanés en La Habana  
    Claves de la nueva Ley General de Comunicación Audiovisual, más allá del enfado de los productores independientes
    Jordi Mollà se encierra con 65 toros de Osborne para pintarlos
    Michael J. Fox, Diane Warren, Peter Weir y Euzhan Palcy recibirán los Oscar honoríficos
    Polémica antisemita en la Documenta: cubren con tela negra un mural que incluye figuras ofensivas para los judíos
    Gengoroh Tagame, de maestro del manga adulto gay a educador sobre el matrimonio igualitario
    El órgano más antiguo del mundo vuelve a vibrar
    Jeffrey Sachs: “Algo falla en el sistema americano. Y en la naturaleza humana”
    Un paseo fluvial con museos y otro lleno de piscinas termales. Las sorpresas de la Vía de la Plata
    Una fuente termal en el centro del pueblo y cómo distinguir a los pájaros por su canto. Las sorpresas del Camino Portugués de la Costa
    El Pirineo oscense, para entrar a vivir
    Olite revive el Medievo para asentarse en el futuro
    Toda la lectura del verano, en el bolsillo
    Libros de intriga que hielan la sangre para combatir el calor
    Diez libros que han cambiado la vida a miles de lectores
    Consigue entradas para el Festival Río Babel
    Disfruta antes que nadie de 'Mali Twist'
    'TINA', el musical de Tina Turner
    'Tartufo' en el Teatre Goya de Barcelona
    José Fernando Molina gusta y abre una generosa puerta grande en su presentación en Madrid
    Escaso (y festivo) público
    Muere el torero Andrés Vázquez a los 89 años de edad
    ¿Podría un juez prohibir los toros en España?
    En los sesenta, todo se vendía con fotos
    De cómo Beyoncé resucitó la música ‘house’
    Lo que siento (no se olviden de Ucrania) 
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Nebrija, el humanista que se enfrentó a la Inquisición
    Un tomo inédito de John Fante, la filosofía de Rüdiger Safranski y otros libros de la semana
    Lucy Ellmann: “Los hombres deberían callarse y dejarnos resolver los problemas”
    Wilco contra el mundo cruel: un nuevo disco delicioso, natural, sencillo y sin sorpresas
    La Documenta sí invita a la lógica
    Mercucio salva la función en el ‘Romeu i Julieta’ de David Selvas
    ‘El amor enamorado’: Eros no sabe querer
    Alex sin Ada
    ¡Alerta naranja!
    La guerra y el mestizaje explicados a mi hijo
    El amor por España de J. B. Trend
    ‘Jung y la imaginación alquímica’, máquinas  de imaginar
    ‘Ser único’, singulares del pensamiento
    ‘La novela ideal’, vida de un vampiro nudista
    ‘Economía en Transición’, el precio de ser europeos
    Óscar Esquivias: “No hace falta ser creyente para leer la Biblia”
    Amelia Castilla: “Los ritos nos ayudan a hacer viable el trance de la muerte”
    Shuarma: “Me gusta de la poesía el silencio que encierra”
    Eva Orúe: “Haría cola por la firma de Margaret Atwood”
    Fernando Castro Flórez: “Mortadelo y Filemón’ es uno de mis ‘textos sagrados”
    Susto en el Mundial de natación: la española Andrea Fuentes rescata a una nadadora que se desmayó en el agua
    Popovici despide a Dressel con un oro histórico en los Mundiales de Natación
    El golf está bañado en oro: de Tiger Woods a la liga saudí
    El ‘Cuerdo’ Bielsa
    El Real Madrid añade más trapío en el éxito
    Antecedentes confirmados
    De lo imposible al cielo
    El Torneo de Candidatos de ajedrez de Madrid, en directo
    Ya casi no hay goles de falta directa, y la culpa no es de los lanzadores
    Nakamura también perdona a Niepómniashi
    El PGA Tour contraataca con más dinero ante la fuga de jugadores a la liga saudí
    Caeleb Dressel abandona los Mundiales de Natación de Budapest
    Pau Gasol critica a Lambán por “politizar” los Juegos y este le pide “informarse mejor”
    Nadal reverdece en Hurlingham
    Laporta pide militancia en el Camp Nou tras la invasión de 30.000 seguidores del Eintracht 
    Juegos 2030: Los audios de las reuniones técnicas entre Cataluña y Aragón dejan entrever que la decisión para bloquearlos fue política
    Videoanálisis | Buscando un rival para Magnus Carlsen en el Torneo de Candidatos 
    Lewandowski desafía al Bayern para jugar en el Barça
    El Athletic decidirá el viernes entre Bielsa o Valverde como entrenador
    Jennifer Hermoso deja el Barcelona y se va al Pachuca
    La nueva gran atracción del fútbol español
    “Nunca acepto un no por respuesta”
    La mayor fábrica de baloncesto de Europa
    Crónica de dos ciudades moldeadas por la misma pasión 
    Niepómniashi castiga la insensatez de Firouzja
    Un viaje de dos meses y medio para escalar la ruta más difícil en Yosemite y fallar en el último movimiento
    Kamikaze Firouzja
    David Ferrer, nuevo director de la Copa Davis
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    Operación Conífera: una decena de detenidos por amañar partidos del fútbol modesto para apuestas
    Jordi Sargatal: “Cuando tienes a alguien como Marc Gasol, tienes que adaptar tus ideas a él”
    Míchel conquista a Guardiola
    ¿Sigue siendo imprescindible tener un antivirus? 
    Google News vuelve a España ocho años después de su cierre
    Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
    Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
    Por qué retuitear el vídeo sexual de Santi Millán también es delito: la desprotección de la intimidad en internet
    LaMDA, la máquina que “parecía un niño de siete años”: ¿puede un ordenador tener conciencia?
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    “Gano 1.500 euros al mes con los videojuegos”: así funciona el negocio de la compraventa de cuentas
    Cinco aplicaciones móviles, con aval científico, que salvan vidas o mejoran tu salud
    Cómo contarle tus ciclos menstruales a una app puede llevarte a la cárcel
    Bill Gates dice que las criptomonedas y los NFT están basados en encontrar a “alguien más tonto”
    El Princesa de Asturias de Investigación Científica distingue a cuatro expertos en sistemas que imitan al cerebro
    Ha llegado el final de Internet Explorer. Y ahora, ¿qué?
    Crece el número de españoles que evitan las noticias duras como la pandemia o la guerra de Ucrania
    Putin, Messi y otros 500 intereses masculinos: así puede explotarse Facebook, “la mayor base de datos de la cultura humana”
    En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
    Instagram, el mejor de los mundos posibles
    Del terrorismo youtuber al influencer rabioso: el odio inunda la red
    Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
    Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
    La solución definitiva para vender más (y mejor) en la web
    La cámara de este ‘smartphone’ es pura magia
    Por qué todos hablan de este ‘smartphone’ de diseño atractivo y rendimiento prémium
    Un campus de programación para adquirir todas las habilidades ‘tech’
    Una catapulta para el talento de ‘kilómetro cero’
    ¿Sigue siendo imprescindible tener un antivirus? 
    Google News vuelve a España ocho años después de su cierre
    Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
    Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
    Por qué retuitear el vídeo sexual de Santi Millán también es delito: la desprotección de la intimidad en internet
    LaMDA, la máquina que “parecía un niño de siete años”: ¿puede un ordenador tener conciencia?
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    “Gano 1.500 euros al mes con los videojuegos”: así funciona el negocio de la compraventa de cuentas
    Cinco aplicaciones móviles, con aval científico, que salvan vidas o mejoran tu salud
    Cómo contarle tus ciclos menstruales a una app puede llevarte a la cárcel
    Bill Gates dice que las criptomonedas y los NFT están basados en encontrar a “alguien más tonto”
    El Princesa de Asturias de Investigación Científica distingue a cuatro expertos en sistemas que imitan al cerebro
    Ha llegado el final de Internet Explorer. Y ahora, ¿qué?
    Crece el número de españoles que evitan las noticias duras como la pandemia o la guerra de Ucrania
    Putin, Messi y otros 500 intereses masculinos: así puede explotarse Facebook, “la mayor base de datos de la cultura humana”
    En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
    Instagram, el mejor de los mundos posibles
    Del terrorismo youtuber al influencer rabioso: el odio inunda la red
    Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
    Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
    La solución definitiva para vender más (y mejor) en la web
    La cámara de este ‘smartphone’ es pura magia
    Por qué todos hablan de este ‘smartphone’ de diseño atractivo y rendimiento prémium
    Un campus de programación para adquirir todas las habilidades ‘tech’
    Una catapulta para el talento de ‘kilómetro cero’
    Guillermo de Inglaterra y Kate Middleton ya tienen su primer retrato oficial con zapatos de Manolo Blahnik y un broche de Isabel II
    Zara Home celebra en París su ambiciosa colaboración con el arquitecto estrella Vincent Van Duysen
    Brad Pitt cree que está llegando el final de su carrera: “De un tiempo a esta parte, me veo ya en mi última etapa”
    Los gestos de Charlene y Alberto de Mónaco en Oslo para zanjar los rumores de crisis
    Javier Olleros, el chef que sirve compost y corteza de árbol quemado: “Hay que acabar con el descontrol de desperdicios y el ritmo frenético”
    Guillermo de Inglaterra cumple 40 años como el candidato ideal para seguir la estela de Isabel II
    Los problemas crecen para los Bieber: Hailey, demandada por la marca de cosmética que lanzó hace una semana
    Shaquille O’Neal, el rey de las franquicias: 155 hamburgueserías, 40 gimnasios y una fortuna de 400 millones
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    Los 40 años de Guillermo de Inglaterra en 16 fotos
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    Mariano Alameda: “Tardé años en librarme de Íñigo”
    La moda masculina toma en Milán las riendas de su propio ‘revival’
    Nicky y Simone Zimmermann: “Nos dijeron que no nos dedicáramos a la moda y que no trabajáramos en familia. No les hicimos caso y nos fue bien”
    Viktor & Rolf, 30 años de moda y rebelión: “No puedes estar siempre arriba”
    Desembarco de celebridades internacionales en Sevilla para el desfile de Dior
    Kim Kardashian causó graves daños al histórico vestido de Marilyn Monroe que llevó en la gala del Met
    Mi extraña nostalgia por Abercrombie & Fitch & lo que fuimos
    La evolución de los modales al comer en la mesa
    Ibiza, entre la noche desenfrenada y el turismo tranquilo 
    Los 33, el nuevo local de tapeo a la brasa con esencia uruguaya en Madrid
    Iñigo Urrechu, cocinero: “Tienes que hacer una cocina instagrameable porque todo el mundo saca pecho de comer en un sitio bonito”
    Un viaje en el tiempo con Kurt Vonnegut
    Muere José Luis Balbín, mítico presentador y creador del programa ‘La clave’
    El TSJ de Madrid declara nulo el despido del guionista de TVE que escribió el rótulo “Leonor se va de España, como su abuelo”
    ‘Supervivientes’ y la incultura general
    ‘Intimidad’ o la denuncia de un delito del siglo XXI 
    ‘Intimidad’, protagonizada por Santi Millán
    En el nombre de Rociito
    ‘Legacy’: un Bosch sin placa y un poco perdido
    Claves de la nueva Ley General de Comunicación Audiovisual, más allá del enfado de los productores independientes
    ‘Sanditon’ resucita a Jane Austen
    Ciencia, tecnología y entrevistas en las novedades de la programación de verano en la Cadena SER
    Los abonados a las plataformas y televisiones de pago superan el número de hogares españoles 
    ‘Intimidad’, protagonizada por Santi Millán
    La historia de Warren Jeffs, un profeta tirano, violador y líder mormón
    ‘Pasapalabra’ busca a su próxima gran estrella
    Mueren en un accidente de tráfico dos actores mexicanos durante el rodaje de la serie de Netflix ‘El Elegido’  
    ‘Intimidad’, violadores y mucho más
    ¿Qué ver hoy en TV? Jueves 23 de junio de 2022
    Nueve capítulos para recordar ‘The Wire’ en su 20º aniversario
    Harry Palmer: el tercer vértice del mágico triángulo de espías británicos
    Las series de junio de 2022: ‘The Boys’ en Amazon Prime Video; ‘Peaky Blinders’ en Netflix y otras
    La fuerza acompaña a ‘Obi-Wan Kenobi’, una serie deslumbrante
    Claves sobre el recibo de la luz: ¿Por qué ha subido? ¿Qué contrato tengo y cuál me conviene?
    El piloto de ‘airbuses’ que se eleva componiendo pop barroco
    Viaje al fin de Occidente, en la gran frontera entre Finlandia y Rusia
    La oficina, concentrada en 14 pulgadas
    Ir a un concierto o pintar nos repara emocionalmente
    Así fue nuestra experiencia de escribirnos con GPT-3, una máquina de inteligencia artificial
    Viktor & Rolf, 30 años de moda y rebelión: “No puedes estar siempre arriba”
    Maggie O’Farrell: “Es fundamental escribir sobre cosas que duelen para que nos sintamos menos solos”
    Hola, desconocido, cuéntanos tu vida
    Ahorro y otras ventajas de las compras de kilómetro cero
    Proyectos sociales de inclusión y empleo para que nadie se quede atrás
    Epidemia de violencia: claves del negocio de las armas en Estados Unidos
    Jorge Drexler: “Fui un ejemplo de fracaso en la industria discográfica durante mucho tiempo”
    La palabra épica
    ‘Influencers’
    Cuento del profesor Pírfano 5
    Harina enriquecida para acabar con el “hambre oculta”
    Lugares de esperanza para salvar los océanos
    Hola, desconocido, cuéntanos tu vida
    Los ejecutivos voladores y la ética medioambiental
    Yaiza Rubio: “Internet ha traído nuevos y muy preocupantes modos de espionaje”
    Los ucranios ya tienen casa en París
    Tenemos que hablar de la alopecia (Jada Pinkett estaría de acuerdo)
    Néstor Pablo Roldán, el ceramista de ‘Los herederos de la tierra’
    Las manos maestras del Palacio Real
    Sergio Hernández: “En el mundo, la gente ya no quiere verdades, quiere mentiras”
    El café de los abuelos o, simplemente, el lugar donde comer las mejores tartas de Viena
    Riesgo, dolor y placer: cómo los humanos se aficionaron al picante 
    Cómo es la vida en un apartamento del siglo XXI... dentro de un palacio decimonónico
    La nueva edad de oro de la coctelería en Barcelona
    El Skoda Karoq reafirma su apuesta de SUV versátil
    Ilusiones hipnóticas
    El poder del hormigón
    Maulévrier, Japón a la francesa
    ‘Fantasías en el Prado’, por Alberto García-Alix
    ¡‘Yee-haw’! Esto también es Brasil
    [1m[34mA continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:[0m
    [1m[32mFeminismo[0m
    Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
    [1m[32mIgualdad[0m
    Un año de eutanasia en España: 172 casos y una gran desigualdad entre las comunidades autónomas
    La escuela concertada ante las desigualdades: el debate pendiente
    [1m[32mMujeres[0m
    Un aula de Vallecas se rebela contra los libros de texto que silencian a las mujeres
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    [1m[32mMujer[0m
    Ellos no bailaron solos: la mujer detrás de la loca historia de Locomía
    ¿La democracia es una sola mujer trabajadora en la Asamblea de Francia?
    El conde de Atarés asesinó a su mujer el día en que se disponía a abandonarle
    La policía detiene a la expareja de una mujer cuyo cadáver fue hallado en el Guadalquivir
    Un aula de Vallecas se rebela contra los libros de texto que silencian a las mujeres
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    [1m[32mBrecha salarial[0m
    
    [1m[32mMachismo[0m
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    [1m[32mViolencia[0m
    “Yo no tuve infancia”: la huida de Catalina de todas las violencias de su vida con solo 16 años
    Armas, nobleza y violencia machista: ¿hay menor percepción de gravedad en las clases socioeconómicas más altas?
    Epidemia de violencia: claves del negocio de las armas en Estados Unidos
    [1m[32mMaltrato[0m
    
    [1m[32mHomicidio[0m
    
    [1m[32mGénero[0m
    Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    [1m[32mAsesinato[0m
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    Hachas, niños y asesinatos bajo césped artificial: así es la necrópolis monumental más antigua de España 
    [1m[32mSexo[0m
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    

## Programación Literaria con Python

### Librerías

Vamos a utilizar las siguientes librerías:

#### Módulos del sistema

- [time](https://docs.python.org/3/library/time.html), este módulo proporciona funciones para trabajar con fechas y/o horas.
- [csv](https://docs.python.org/3/library/csv.html), implementa clases para leer y escribir datos tabulares en formato CSV.
- [re](https://docs.python.org/3/library/re.html), proporciona operaciones de coincidencia de expresiones regulares similares a las que se encuentran en Perl.
- [os](https://docs.python.org/3/library/os.html), El módulo proporciona una forma portátil de usar la funcionalidad dependiente del sistema operativo.

#### Librerías Externas

- [requests](https://requests.readthedocs.io/en/latest/), librería de Python para trabajar con HTTP.
- [bs4](https://pypi.org/project/beautifulsoup4/), se utiliza para extraer datos de archivos HTML y XML.
- [pandas](https://pandas.pydata.org/), es una herramienta de manipulación y análisis de datos de código abierto rápida, potente, flexible y fácil de usar.
- [termcolor](https://pypi.org/project/termcolor/), se trata de una libreria que permite imprimir texto coloreado.

#### Instalamos librerias

Las librerías que vienen con Python no requieren instalarse, pero el resto sí.


```python
pip install requests bs4 pandas termcolor
```

#### Importamos librerias

Hay librerías que las importamos tal cual, como el caso de `requests`, otras que se importan cambiándoles el nombre que se va a utilizar para invocarlas, como es el caso de `pandas` y otras de las cuales importamos algunos componentes, como es el caso de `bs4` y `termcolor`:

import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
```

### Objetos/Variables

Vamos a crear una serie de objetos o variables:

#### Resultados 

Creamos un objeto vacío denominado `resultados` en el que se añadirán los resultados del __scraping__.


```python
resultados = []
```

Si le paso la función `type()` veremos que se trata de un objeto de tipo `list` o "lista" de Python. Se trata de un elemento básico para la organización de datos o información.


```python
type(resultados)
```




    list



#### Para acceder a los datos de un sitio 

Aquí se agrega variable con la que se solicita recoger información de la URL del sitio.


```python
req = requests.get("https://resultados.elpais.com")
```

Al pasar la función `type()` se observa que es un objeto de tipo Respuesta modelo `requests`.


```python
type (req)
```

En el código vemos que se usa el condicional `if` para que no pueda leerse el valor de vuelta en caso que el estatus no sea 200, lo que significa: solicitud exitosa. Cuando el resultado no se encuentra se mostraria un mensaje donde se dice que _No se puede hacer web scraping_ de la URL equivocada.


```python
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
```

En otro caso, al pasar la función `type()` se observa que el objeto ` req.status_code ` dará un resultado numérico porque es de tipo _entero_.

#### Beautiful Soup

Esta variable se utiliza para hacer el proceso de web scraping.


```python
soup = BeautifulSoup(req.text, 'html.parser')
```

Cuando pasamos la función `type()` nos damos cuenta que se trata de un objeto de tipo `bs4`, librería que permite extraer información en formatos html o xml.


```python
type(soup)
```


```python
bs4.BeautifulSoup
```

Luego se debe agregar una variable para encontrar las etiquetas de tipo h2 dentro de la `URL` en la que se quiere hacer web scraping.


```python
tags = soup.findAll("h2")
```

Al pasar la funcion `type()` vemos un objeto `tags` de tipo resultados.


```python
type(tags)
```


```python
bs4.element.ResultSet
```

A traves de un `for` se le ordena recorrer todos los `h2` y que se imprima la informacion contenida dentro de la etiqueta. Los resultados son agregados dentro de la lista con resultados.append(h2.text)


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

Aquí observamos que al pasar la funcion `type()` el objeto resultados.append es de tipo metodo integrado.


```python
type(resultados.append)
```

El uso de funciones y elementos es igual para cada ciclo. En el ejercicio para esta tarea, también se permite la impresión de informacion mas precisa para cada sección del sitio web en cuestión.

### Para esta tarea

Debo reconocer que el desarrollo de ejercicios de programación literaria ha sido de las tareas más complejas, pues un área de la que no conocía a profundidad en el ejercicio de mis labores habituales.

Se trata de una experiencia interesante, que realizo por primera vez, y que demanda de uno el prestar atención a lo que se está haciendo y de qué manera funciona en la práctica.


```python

```
