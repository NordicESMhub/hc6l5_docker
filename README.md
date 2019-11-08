# hc6l5_docker
CESM historic with CAM6 and CLM5 (no ocean)

CESM docker container for HIST_CAM60_CLM50%BGC_CICE%PRES_DOCN%DOM_MOSART_CISM2%NOEVOLVE_SWAV  compset and resolution f19_g17 using [bioconda cesm docker](https://bioconda.github.io/recipes/cesm/README.html) as a base image.

- Input dataset is stored and available in zenodo.

**TBD**: once transfered is finalized, we need to update this section!


## Running hc6l5  with docker

Make sure inputdata is available (it won't download it as we suppose it is already on disk). 
- The location of the inputdata is `/opt/uio/inputdata` 
- Model outputs are stored in `/opt/uio/archive` along with the `case` folder (it can be interesting to check timing).

```
docker pull nordicesmhub/cesm_hc6l5:latest
docker run -i -v /opt/uio/inputdata:/home/cesm/inputdata -v /opt/uio/archive:/home/cesm/archive  -t nordicesmhub/cesm_hc6l5:latest
```


