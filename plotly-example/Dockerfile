FROM jupyter/minimal-notebook

RUN pip install numpy==1.16.4 
RUN pip install matplotlib==3.1.0

RUN pip install plotly==3.10.0
RUN pip install jupyterlab==0.35 "ipywidgets>=7.2"

RUN export NODE_OPTIONS=--max-old-space-size=4096 \
  && jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.38 --no-build \
  && jupyter labextension install plotlywidget@0.11.0 --no-build \
  && jupyter labextension install @jupyterlab/plotly-extension@0.18.2 --no-build \
  && jupyter labextension install jupyterlab-chart-editor@1.1 --no-build \
  && jupyter lab build \
  && unset NODE_OPTIONS

RUN pip install pandas==0.24.2
RUN pip install scipy
