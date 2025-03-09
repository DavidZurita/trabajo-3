FROM mcr.microsoft.com/devcontainers/anaconda:1-3

# Copy environment.yml (if found) to a temp location so we update the environment. Also
# copy "noop.txt" so the COPY instruction does not fail if no environment.yml exists.
COPY environment.yml* .devcontainer/requirements.txt  /tmp/conda-tmp/

# Crear un nuevo entorno e instalar las dependencias desde el archivo requirements.txt
RUN conda create --name trabajo3 --file /tmp/conda-tmp/requirements.txt \
    && rm -rf /tmp/conda-tmp

# Instalar ipykernel en el entorno trabajo3
RUN conda install -n trabajo3 ipykernel --update-deps --force-reinstall

# Establecer el entorno por defecto al iniciar el contenedor
# RUN echo "conda activate trabajo3" >> ~/.bashrc

# Establecer el entorno por defecto al iniciar el contenedor
RUN echo "source activate trabajo3" > ~/.bashrc

# Exponer el puerto que usa Jupyter Notebook
EXPOSE 8888

# Comando para iniciar Jupyter Notebook con el kernel de Conda
CMD ["sh", "-c", "source activate trabajo3 && jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root"]



# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>



