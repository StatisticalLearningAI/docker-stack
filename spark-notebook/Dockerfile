FROM jupyter/datascience-notebook

USER $NB_UID

# Install Python 3 packages
RUN conda install --quiet --yes \
    'psycopg2=2.8.*' \
    'pyspark=2.4.*'

# Install Tensorflow
RUN pip install --quiet \
    'tensorflow==2.1.0' && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER