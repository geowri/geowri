# Bem-vindo ao GitHub da WRI - Equipe de Ciência de Dados

## Sobre Nós
A WRI (World Resources Institute) é uma organização global que busca soluções inovadoras para desafios ambientais críticos. Nossa equipe de **Ciência de Dados** se dedica ao **geoprocessamento** e à análise de grandes volumes de dados geoespaciais, utilizando tecnologias de ponta para transformar dados em insights práticos.

## Foco Principal
No GitHub da nossa equipe, você encontrará ferramentas, scripts e projetos voltados para:
- **Geoprocessamento com Python**: Automação e processamento de dados geoespaciais usando bibliotecas como **GDAL**, **Geopandas** e **Shapely**.
- **Análise de Dados Geoespaciais**: Soluções para lidar com dados raster e vetoriais em grande escala.
- **Scripts de Modelagem e Reprojeção de Dados**: Scripts para conversão de formatos, reprojeção de shapefiles e rasters, mosaicos e cálculos avançados com dados de satélite.

## Tecnologias que Utilizamos
- **Python**: Para automação e manipulação de dados geoespaciais.
- **GDAL**: Ferramenta poderosa para manipulação e conversão de dados raster e vetoriais.
- **PostGIS**: Extensão espacial do PostgreSQL para armazenamento e consulta de dados geográficos.
- **QGIS**: Integração de scripts e análises para uso em plataformas de SIG.

## Exemplos de Repositórios
- **Scripts para GDAL**: Automação de processos como reprojeção, mosaicos e cálculos em dados raster.
- **Ferramentas de Análise Espacial**: Scripts para análise de cobertura do solo, cálculo de áreas restauradas e análise de biodiversidade.
- **Integração com Banco de Dados Geoespaciais**: Scripts para conectar e trabalhar com **PostGIS** e **GeoServer**.

## Como Contribuir
Se você trabalha com **ciência de dados geoespaciais** ou está interessado em contribuir com projetos de **geoprocessamento**, este é o lugar certo! Explore nossos repositórios, abra *issues*, sugira melhorias ou faça um *fork* para contribuir com código.

## Contato
Para mais informações sobre os projetos de geoprocessamento da WRI, entre em contato com a equipe de ciência de dados ou visite nosso [site oficial](https://geowri.org).

## Script de Instalação do Anaconda e Configuração de Ambiente Geoespacial

Este script automatiza a instalação do Anaconda e a configuração de um ambiente com pacotes geoespaciais e científicos.

### Etapas do Script:

1. **Baixar a versão mais recente do instalador do Anaconda**  

```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh
```

2. **Alterar permissões do instalador para torná-lo executável**  

```bash
sudo chmod u+x Anaconda3-2024.06-1-Linux-x86_64.sh
```

3. **Executar o script de instalação do Anaconda certifique-se de seguir as instruções interativas**

```bash
./Anaconda3-2024.06-1-Linux-x86_64.sh
```

4. **Ativar o Anaconda no terminal**  

```bash
source ~/anaconda3/bin/activate
```

5. **Criar um ambiente chamado 'geowri'**  
Este ambiente será utilizado para trabalhar com bibliotecas geoespaciais e científicas:

```bash
conda create -n osgeo python=3.10 -y
```

6. **Ativar o ambiente 'osgeo'**:

```bash
conda activate osgeo
```

7. **Instalar pacotes geoespaciais e científicos via conda-forge**  
Instalar uma lista de pacotes que cobrem diversas funcionalidades, como processamento de dados raster, machine learning, entre outros:

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

9. **Confirmar a configuração do ambiente**  
Verificar se as principais bibliotecas estão instaladas e funcionando:

```bash
python -c "import geopandas, rasterio, gdal, numpy; print('Ambiente configurado com sucesso!')"
```

### Instruções Finais:
- Para ativar o ambiente `osgeo` no futuro, use o comando:

```bash
conda activate osgeo
```

- Para desativar o ambiente, use:

```bash
conda deactivate
```

