# **Women in Bioinformatics and Data Science**
## 2023 1st WBDS LA Camp "Introduction to Bioinformatics and Data Science"** 
## Proyecto final elaborado por Norma Paulina López Zamora para el Bootcamp "Women in bioinformatics and Data Science"

 A la fecha, se ha caracterizado gran diversidad de géneros bacterianos que tiene la capacidad de fijar nitrogeno y producir compuestos que estimulan el crecimiento vegetal. El género *Pseudomonas* ha sido ampliamente estudiado por su capacidad de excretar metabolitos secundarios que han demostrado ser efectvios en el biocontrol (Bonaterra, et al. 2022). 

Para este proyecto se hará uso de las siguientes bibliotecas, que se pueden instalar con el comando !pip3 install
```
- !pip3 install matplotlib
- !pip3 install requests
- !pip3 install matplotlib
- !pip3 install pandas
- !pip3 install pycirclize
- !pip3 install pyrodigal
- !pip3 install requests
- !pip3 install seaborn
- !pip3 install biopython
```

Las bibliotecas que usaremos son las siguientes:


-  [pandas](https://pandas.pydata.org/) para el manejo general de datos
- [pyCirclize](https://moshi4.github.io/pyCirclize/) para visualizar nuestros datos genómicos
- [pyrodigal](https://pyrodigal.readthedocs.io/en/stable/) para la predicción de genes codificantes
- [requests](https://requests.readthedocs.io/en/latest/) para interactuar con las APIs de NCBI, UniProt 
- [seaborn](https://seaborn.pydata.org/) para visualizar algunas de las propiedades genómicas obtenidas
- [subprocess](https://docs.python.org/3/library/subprocess.html) ejecutar comandos fuera del entorno de python
- [BioPython](https://biopython.org/) para el manejo de secuencias
- [io](https://docs.python.org/3/library/io.html) para conectar las entradas y salidas de los distintos programas

Importemos las librerías que vamos a usar con el siguiente código:
```
import matplotlib.pyplot as plt
import numpy  as np
import pandas as pd
import pyrodigal
import requests
import seaborn as sns
import subprocess
import sys
from Bio import SeqIO
from Bio import Entrez
Entrez.email   = "aquí va tu correo"
Entrez.api_key = "aquí va el código del API key"
from io                 import StringIO
from matplotlib.patches import Patch
from pycirclize         import Circos
from pycirclize.parser  import Gff
from requests.adapters  import HTTPAdapter, Retry

```

Debes registrarte con tu correo electrónico y obtener la API key que proporciona NCBI a sus usuarios registrados (más información de como obtener una API key [aquí](https://support.nlm.nih.gov/knowledgebase/article/KA-05317/en-us)
