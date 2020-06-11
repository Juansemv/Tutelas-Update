# Exigiendo ciudadanía: Análisis tutelar en temas de salud (1992 - 2019).
---
##### 22 de noviembre de 2019

Autor: <a href="https://www.linkedin.com/in/sebastianmunozv/">Juan Sebastian Muñoz Vargas</a>

Objetivo: Analizar, históricamente, el uso del lenguaje y los cambios en la tutelación referente a temas de salud de 1992 - 2019.

![Nube de palabras](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Nube/WordCloud_Health.png)

## Descripción y motivación

Los derechos sobre la salud son los segundos más aclamados en todo el ejercicio tutelar, representando el 29.8% de todas las tutelas (a 2017). Siendo así, el presente trabajo tiene contemplado recolectar de forma automática las casi 6.000 tutelas relativas a temas de ‘salud’ publicadas en la <a href="http://www.corteconstitucional.gov.co/relatoria/radicador/buscar.php?ponente=&demandado=&Sentencia=&Tipo=Sentencias&busqueda=salud&conector=AND&segundotema=&anios=Todos&pg=0&vs=0&accion=Buscar">página de la Corte Constitucional</a>. Con el objetivo de comprender cómo las tutelas relativas a la salud se han transformado y reflejan los procesos políticos y sociales en el momento de su escritura.

Las preguntas que guían el presente trabajo son las siguientes:

* ¿Cuáles son las principales demandas ciudadanas en temas relativos a la salud?
* ¿Quiénes son los actores mayormente demandados por temas de salud en el país?
* ¿Cuáles años son los años con mayor cantidad de sentencias?
* ¿Cuáles son los temas principales presentes en estas tutelas?
* ¿Cuáles son los magistrados que más presentan tutelas relativas a salud?
* ¿La cantidad de tutelas es un indicador de la relevancia mediática de algunos temas?
* ¿Son los cambios gubernamentales una razón de cambio en el ejercicio tutelar?
* ¿Que rol juegan ciertos conceptos en la escritura de tutelas?

## Métodos usados
### 1. Web Scraping

- Se realizó la extracción de las tutelas de la <a href="http://www.corteconstitucional.gov.co/relatoria/radicador/buscar.php?ponente=&demandado=&Sentencia=&Tipo=Sentencias&busqueda=salud&conector=AND&segundotema=&anios=Todos&pg=0&vs=0&accion=Buscar">página oficial de la Corte Constitucional</a>, al realizar la búsqueda de sentencias con la palabra "salud". De allí, se extraen 5837 tutelas.

- Se hace uso de las siguientes librerias:
   - 'Requests'
   - 'Beautiful soup'
   - 'Regex'
- Gracias a los métodos anteriores, se obtiene de la tutela: El número de Item, Expediente, Año, Mes , Día , Link a la sentencia, Número de la sentencia, Magistrado Ponente, Demandante, Demandado y Tema.

** El código se encuentra disponible <a href="https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Code-%20PF.ipynb">acá</a>.

### 2. Limpieza  y gestion de la base de datos
- Se hizo uso de 'Pandas' para organizar la información en formato de base de datos y se almacenó en formato 'Pickle'.
- Se usaron las librerias 'regex, 'string' y 'nltk' para eliminar la puntuación, pasar a minúscula, eliminar palabras vacías, etc. 

** El código se encuentra disponible <a href="https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Limpieza.ipynb">acá</a>.

## Resultados:

** El código se encuentra disponible <a href="https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/An%C3%A1lisis%20de%20Tutelas.ipynb">acá</a>.

* Cantidad de tutelas disponibles: 5837
* Día con más tutelas: 16 de Junio de 2010
* Mes con mayor cantidad de tutelas: Octubre
* Año con mayor cantidad de tuelas: 2008

### Algunas visualizaciones:
![Barras_mes](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/barras_mes.png)
![Barras_Magistrado](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/barras_magistrado.png)
#### Las líneas rojas marcan el cambio presidencial
![Barras_Años](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/barras_a%C3%B1os.png)
![Linea_mes](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/linea_mes.png)
![KW_Conclicto](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/KW_Conflicto.png)
![KW_EPS__Medicamentos](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/KW_EPS_Medicamentosey_words1_month.png)
![Medicamentos](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/medicamentos.png)
Uso de la palabra dignidad:

![Dignidad](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/Dignidad.png)

Uso de la palabra seguridad:

![Seguridad](https://github.com/Juansemv/MCPP_juan.munoz/blob/master/Proyecto%20final/Gr%C3%A1ficos/Seguridad.png)
##### ¡Gracias!
