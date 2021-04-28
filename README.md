# Assignment 3: Building Visual Apps to Explore Fake Scientific People and Literature using Data Science: Creating Data Insights

Due: Friday, April 30, 2021 12pm PT

fryt@usc.edu

https://1.bp.blogspot.com/-TaCRW57W7Oo/WvFFHYxupmI/AAAAAAAAEbU/DztKBGpxjXkZo99wBRRs01k_f2bDrsPogCLcBGAs/s1600/Trinity%2Bxfce%2Bhackers%2Bthemes.png


### Technologies
* D3 v2, v3
* Elasticsearch v7.12.0


## 1. Convert TSV to Json
Execute ```tsvtojson.py```:
```python
python tsvtojson.py data/assignment1.tsv
python tsvtojson.py data/assignment2.tsv
```

## 2. Generate D3 Visualizations
Resources:
* https://github.com/d3/d3/wiki/Gallery
* https://www.jasondavies.com/wordcloud/
* https://gist.github.com/ericcoopey/6382449
* http://bl.ocks.org/jhb/5955887
* http://bl.ocks.org/fancellu/2c782394602a93921faff74e594d1bb1
* https://bost.ocks.org/mike/miserables/

### 2.1. [Wordcloud](https://www.jasondavies.com/wordcloud/)
Wordcloud of common words of (1) all original messages, (2) original messages by attack type, (3) all generated messages, (4) generated messages by attack type

### 2.2. [Force Layout Graph](http://bl.ocks.org/jhb/5955887)
Nodes and edges between sender IP geolocation and TIKA Geoparser geolocations of all original messages

### 2.3. [Co-Occurrence](https://bost.ocks.org/mike/miserables/)
Co-occurrence of features over all original messages

## 3. Ingest into Elasticsearch
Resources:
* https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html

### 3.1. Pull and run docker image
```bash
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.12.0
```

## 4. Imagespace
Resources:
* https://github.com/nasa-jpl-memex/image_space/wiki/Quick-Start-Guide-with-ImageCat
