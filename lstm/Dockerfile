# Pull anaconda with python3 image
FROM continuumio/anaconda3:latest

# Update the image
RUN apt-get update \
&& apt-get -y upgrade

# Update Anaconda and install deep learning frameworks theano, keras and tensorflow
# Create user to run notebook, create password "workshop" for the jupyter server
RUN /opt/conda/bin/conda update anaconda \
&& /opt/conda/bin/conda install theano \
&& /opt/conda/bin/conda install -c conda-forge tensorflow \
&& /opt/conda/bin/conda install jupyter -y --quiet \
&& /opt/conda/bin/conda install -c conda-forge keras \
&& useradd --create-home --home-dir /home/condauser --shell /bin/bash condauser \
&& mkdir /home/condauser/.jupyter \
&& printf "c.NotebookApp.password = u'sha1:83aab2852741:71a56c4865ed39886d3742c4aac07fdd64489627'" > /home/condauser/.jupyter/jupyter_notebook_config.py \
&& chown condauser:condauser /home/condauser -R

# Change to condauser
USER condauser

# Set the working directory
WORKDIR /home/condauser

# The port to expose from this container
EXPOSE 8888

# Run the jupyter notebook server when the container starts. Password "workshop"
CMD /opt/conda/bin/jupyter notebook --notebook-dir=/home/condauser --ip='*' --port=8888 --no-browser
