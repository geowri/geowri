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

## Instalação

Instruções para instalar o RSGISLib:

```bash
conda install -c conda-forge rsgislib
```

Se você deseja instalar um conjunto de pacotes para realizar sensoriamento remoto e análise de dados GIS em Python, os seguintes pacotes são o que eu instalo como ambiente base:

```bash
conda install -c conda-forge rsgislib gdal libgdal-arrow-parquet libgdal-fits libgdal-grib libgdal-hdf4
```

Eu às vezes encontrei conflitos entre pacotes dos canais `default` e `conda-forge` do conda, então recomendo remover o canal `default` da sua configuração e usar apenas o `conda-forge`.

Também instalo os seguintes pacotes usando pip, que não estão disponíveis via conda:

```bash
pip install gsutil alphashape pysptools matplotlib-scalebar pysondb BorutaShap PyMuPDF mpl-scatter-density
```

