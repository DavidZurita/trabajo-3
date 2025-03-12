 ¿Cómo crear entornos conda a partir de un .txt o un .yml?
 
>[!Note]
>Para archivo .txt 
>Para crear el entorno Conda, primero se debe de asegurar que el archivo tenga los paquetes necesarios. En este caso el archivo de configuración .txt contiene lo siguiente:
>   python=3.12.7
>   numpy
>   pandas
>   matplotlib
>   seaborn

> [!Tip]
>Después se debe ejecutar el siguiente comando en el terminal
>   conda create –-nombre entorno --requirements.txt
>Con esto se creará el entorno llamado “nombre entorno” con los paquetes especificados en el archivo .txt

>[!Note]
>Para archivo .yml
>Es muy similar, primero debemos tener preparado el archivo .yml, mismo que debe tener los paquetes necesarios.
>name: entorno dependencies:
>   python=3.12.7
>   numpy
>   pandas
>   matplotlib
>   seaborn

> [!Tip] 
>Después se debe ejecutar el siguiente comando en el terminal
>   conda env create -f entorno.yml
>Tras ejecutar el comando, se creará un entorno Conda con la configuración especificada en el archivo .yml, en este caso “entorno.yml.”

> [!IMPORTANT]
> Una vez cargado el docker con la imagen preconfigurada se debe realizar las siguientes acciones con la finalidad de trabajar con jupyter notes: <br/>
> Ejecutar en la terminal el siguiente comando: jupyter notes
>Una vez cargado el jupyter, se debe ejecutar el comando: 
>jupyter server list
>Este comando despliega la dirección del jupyter con el token respectivo; para iniciar a realizar los trabajos respectivos se debe copiar el enlace resultante.
>Ejemplo: "http://localhost:8888/?token=7a9e23431312f878fc4946782dbdfa0186ee0d8487103d2c"