# Bem-vindo ao GitHub do WRI Brasil #

## Equipe de Ciência de Dados ##

### Preparação do Ambiente

1. **Baixar a versão mais recente do instalador do Anaconda**  
O link para instalador mais recente pode ser encontrado em [Anaconda](https://www.anaconda.com/download/success).
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh
```

2. **Alterar permissões do instalador para torná-lo executável**  

```bash
sudo chmod u+x Anaconda3-2024.06-1-Linux-x86_64.sh
```

3. **Executar o script de instalação do Anaconda certificando-se de seguir as instruções interativas**

```bash
./Anaconda3-2024.06-1-Linux-x86_64.sh
```

4. **Ativar o Anaconda no terminal**  
Caso tenha escolhido outro caminho, altere.
```bash
source ~/anaconda3/bin/activate
```

5. **Criar um ambiente chamado 'geowri'**  
Este ambiente será utilizado para trabalhar com bibliotecas geoespaciais e científicas:

```bash
conda create -n geowri python=3.12 -y
```

6. **Ativar o ambiente 'geowri'**:

```bash
conda activate geowri
```

7. **Instalar pacotes geoespaciais e científicos via conda-forge**  

```bash
conda install -c conda-forge \
  rsgislib gdal libgdal-arrow-parquet libgdal-fits libgdal-grib libgdal-hdf4 \
  libgdal-hdf5 libgdal-jp2openjpeg libgdal-pg libgdal-kea libgdal-netcdf proj-data \
  geos gsl kealib xerces-c muparser boost-cpp rios scikit-learn scikit-image \
  imbalanced-learn scikit-plot scikit-fuzzy bayesian-optimization optuna matplotlib \
  pandas geopandas statsmodels h5py scipy rasterio shapely networkx sqlalchemy \
  pycurl xgboost catboost lightgbm numba pip sphinx elevation rtree tqdm jinja2 \
  keras parallel bokeh pygal jupyterlab psutil pysal libpysal esda pyyaml netcdf4 \
  xarray rasterstats fiona plotly python-kaleido pyod psycopg2 contextily cvxopt \
  feather-format openpyxl SALib xlsxwriter black jupyterlab_code_formatter ruff \
  flake8 pylint isort autopep8 pytest pytest-html coverage pytest-cov requests \
  imageio Pillow pyyaml exiftool scikit-gstat tuiview -y
```

8. **Atualizar todos os pacotes**  
Garantir que as versões mais recentes estão instaladas:

```bash
conda update -c conda-forge --all -y
```

### Instruções Finais:
- Para ativar o ambiente `geowri` no futuro, use o comando:

```bash
source ~/anaconda3/bin/activate
conda activate geowri
```

- Para desativar o ambiente, use:

```bash
conda deactivate
```

# Alias para ativar o ambiente Conda
```bash
alias geowri='source ~/anaconda3/bin/activate && conda activate geowri'
alias no_geowri='conda deactivate && conda deactivate'
```
