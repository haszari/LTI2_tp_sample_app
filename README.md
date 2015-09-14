## LTI2 sample code -- sample Tool Provider app (i.e. non-LMS side)

This is forked from the @vitalsource repos. I have forked to get things working out of the box - there were various issues getting a dev build running.

To get up and running:
- get a VM running ruby, rails etc 
- clone LTI2 gem and sample apps next to each other in a folder:
  - clone haszari/LTI2-Reference
  - clone haszari/LTI2_tc_sample_app
  - clone haszari/LTI2_tp_sample_app
- get tool consumer app running
  - `cd` into `/LTI2_tc_sample_app` 
  - initialise TC database: `rake init_task:backup`
  - start server: `rails s -p 4000 -e sqlite3 -e development`
- get tool provider app running
  - `cd` into `/LTI2_tp_sample_app` 
  - initialise TC database: `rake init_task:backup`
  - start server: `rails s -p 5000 -e sqlite3 -e development`
