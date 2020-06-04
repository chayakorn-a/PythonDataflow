# Compile Dataflow Template

# with requirements file
python JsonToCsv.py \
    --runner DataflowRunner \
    --project {project_id} \
    --staging_location gs://alex_dataflow_staging/ \
    --temp_location gs://alex_dataflow_temp/ \
    --template_location gs://alex_dataflow_template/MyTemplate \
    --requirements_file requirements.txt \
    --save_main_session True

# with setup file
python JsonToCsv.py \
    --runner DataflowRunner \
    --project {project_id} \
    --staging_location gs://alex_dataflow_staging \
    --temp_location gs://alex_dataflow_temp \
    --template_location gs://alex_dataflow_template/MyTemplate \ <!-- The location where the template file is going to be saved !-->
    --setup_file /Users/{FULL PATH TO SETUP}/setup.py \ <!-- Your local path to setup.py !-->
    --save_main_session True