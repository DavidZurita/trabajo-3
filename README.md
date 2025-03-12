 ¿Cómo crear entornos conda a partir de un .txt o un .yml?
 
[!Note]
Para archivo .txt 
Para crear el entorno Conda, primero se debe de asegurar que el archivo tenga los paquetes necesarios. En este caso son:
git
numpy
pandas
matplotlib
seaborn

[!Tip]
Después se debe ejecutar el siguiente comando en el terminal

conda create –-nombre entorno --requirements.txt

Con esto se creará el entorno llamado “nombre entorno” con los paquetes especificados en el archivo .txt

Para archivo .yml
Es muy similar, primero debemos tener preparado el archivo .yml, mismo que debe tener los paquetes necesarios.

name: entorno dependencies:

numpy
pandas
matplotlib
seaborn

[!Tip] 
Después se debe ejecutar el siguiente comando en el terminal

conda env create -f entorno.yml

Tras ejecutar el comando, se creará un entorno Conda con la configuración especificada en el archivo .yml, en este caso “entorno.yml.”

[!]