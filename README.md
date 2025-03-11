# ¿Cómo crear entornos conda a partir de un .txt o un .yml? 

 

Para archivo .txt 

 

Para crear el entorno Conda, primero se debe de asegurar que el archivo tenga los paquetes necesarios. En este caso son: 
 
<img width="421" alt="image" src="https://github.com/user-attachments/assets/068c4b10-dc40-495e-9c32-0aab832481e1" />


numpy  

pandas  

matplotlib  

seaborn 


Después se debe ejecutar el siguiente comando en el terminal 

conda create –-nombre entorno --requirements.txt 

Con esto se creará el entorno llamado “nombre entorno” con los paquetes especificados en el archivo .txt  

 

 

Para archivo .yml 

Es muy similar, primero debemos tener preparado el archivo .yml, mismo que debe tener los paquetes necesarios.  

name: entorno 
dependencies: 
  - numpy 
  - pandas 
  - matplotlib 

 

Después se debe ejecutar el siguiente comando en el terminal 

conda env create -f entorno.yml 

Tras ejecutar el comando, se creará un entorno Conda con la configuración especificada en el archivo .yml, en este caso “entorno.yml.” 
