#######################################################################################
## DO NOT EDIT THIS FILE! This file was automatically generated from the dockerfile. ##
## Run dynwrap:::.container_dockerfile_to_singularityrecipe() to update this file.   ##
#######################################################################################

Bootstrap: shub

From: dynverse/dynwrap:py2.7

%labels
    version 0.1.5

%files
    . /code

%post
    chmod -R 755 '/code'
    pip install setuptools
    git clone https://github.com/SheffieldML/GPy.git && \
      cd GPy && \
      python setup.py develop && \
      cd ..
    git clone https://github.com/mzwiessele/topslam.git && \
      cd topslam && \
      python setup.py develop && \
      cd ..

%runscript
    exec python /code/run.py

