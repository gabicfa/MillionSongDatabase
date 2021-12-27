# Million song database

<img src="https://github.com/marcelogdeandrade/MillionSongDatabase/blob/master/images/dashboard.png" alt="drawing" width="800"/>

## Data reading and analysis
Data reading and analysis done using Spark can be seen in the `LeituraDeDados.json` file. To view the file, import it into Apache Zeppelin with a notebook. Raw data is acquired from the `millionsongsample2` AWS S3 bucket, previously taken from the 1GB sample of the Million Song Dataset.

To solve the problem of reading the HDF5 file in Spark, the files were converted to TXT locally using the script `TransformHd5ToTxt.json`

Analyzes can also be done using the python scripts from the `python_scripts/` folder. The spark must be configured to have access to AWS S3.

## Dashboard

The dashboard was made using the React frontend framework, based on the Razzle boilerplate. To import the data, we hosted the data analysis output file in the service [mysjon](http://myjson.com/), change the link being imported in the Home component to change the dashboard input data.

To run the dashboard, go into the Dashboard directory and run `$npm install` to install the necessary dependencies. Then run `$npm start` to start the project. To run the production version, run the project build with `$npm run build` and then `$npm run start:prod`

Created at 2017.1
