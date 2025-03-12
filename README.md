 ¿Cómo crear entornos conda a partir de un .txt o un .yml?
 

Para archivo .txt <br/>
Para crear el entorno Conda, primero se debe de asegurar que el archivo tenga los paquetes necesarios. En este caso el archivo de configuración .txt contiene lo siguiente: <br/>
   python=3.12.7 <br/>
   numpy <br/>
   pandas <br/>
   matplotlib <br/>
   seaborn <br/>

> [!Tip]
>Después se debe ejecutar el siguiente comando en el terminal <br/>
>   conda create –-nombre entorno --requirements.txt <br/>
>Con esto se creará el entorno llamado “nombre entorno” con los paquetes especificados en el archivo .txt <br/>
<br/>

Para archivo .yml <br/>
Es muy similar, primero debemos tener preparado el archivo .yml, mismo que debe tener los paquetes necesarios. <br/>
name: entorno dependencies: <br/>
    python=3.12.7 <br/>
    numpy <br/>
    pandas <br/>
    matplotlib <br/>
    seaborn <br/>

> [!Tip] 
>Después se debe ejecutar el siguiente comando en el terminal <br/>
>   conda env create -f entorno.yml <br/>
>Tras ejecutar el comando, se creará un entorno Conda con la configuración especificada en el archivo .yml, en este caso “entorno.yml.”

> [!IMPORTANT]
> Una vez cargado el docker con la imagen preconfigurada se debe realizar las siguientes acciones con la finalidad de trabajar con jupyter notes: <br/>
> Ejecutar en la terminal el siguiente comando: jupyter notes
>Una vez cargado el jupyter, se debe ejecutar el comando: <br/>
>jupyter server list <br/>
>Este comando despliega la dirección del jupyter con el token respectivo; para iniciar a realizar los trabajos respectivos se debe copiar el enlace resultante. <br/>
>Ejemplo: "http://localhost:8888/?token=7a9e23431312f878fc4946782dbdfa0186ee0d8487103d2c"


> [!CAUTION]
> Errores encontrados <br/>
Errores encontrados en el ejercicio Opción 2 <br/>
Error 1: "ModuleNotFoundError: No module named 'seaborn'", esto lo resolvimos con el comando pip install seaborn.

> [!WARNING]
> Mensaje de aviso por cambios futuros <br/>
/tmp/ipykernel_6229/2243821585.py:6: FutureWarning: 'H' is deprecated and will be removed in a future version, please use 'h' instead.
  'timestamp': pd.date_range(start='2023-01-01', periods=10, freq='H'),