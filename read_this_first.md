## Explanations for each directory
updated last on 11/9/2020

### geotracknet/ais_spatial_joins/

- Contains geojson & csv outputs from unique runs of __spatial_join_code/ports_pipeline.ipynb__
- This data is also populating the PostGIS table __public.area_of_interest__

### geotracknet/sagemaker_code/

- Code repo/backup for anomaly detection
- This code is accessed via a SageMaker LifeCycle Management script and implemented via a cronscript on the instance __anomaly-dev-ml-m5-4xlarge__
- Configuring this inside SageMaker is a trial and error hack and this system needs to migrate.
- ___BE CAREFUL___ if trying to restart the instance. This will disconfigure the papermill script from the appropriate conda environment running crontab, and therefore the pipeline.

### geotracknet/sagemaker_output/

- Contains geojson & csv outputs from recurrent runs of __sagemaker_code/divergent_behavior_model_production.ipynb__ 
- This data is also populating the PostGIS table __public.area_of_interest__

### geotracknet/spatial_join_code/

- A boilerplate script for spatial_joins is backed up here __spatial_join_code/ports_pipeline.ipynb__
