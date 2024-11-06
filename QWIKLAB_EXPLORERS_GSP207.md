# Dataflow: Qwik Start - Python || [GSP207](https://www.cloudskillsboost.google/focuses/1100?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

### Run the following Commands in CloudShell

```
export REGION=
```
```
gcloud config set compute/region $REGION

gsutil mb gs://$DEVSHELL_PROJECT_ID-bucket/

gcloud services disable dataflow.googleapis.com

gcloud services enable dataflow.googleapis.com

docker run -it -e DEVSHELL_PROJECT_ID=$DEVSHELL_PROJECT_ID -e REGION=$REGION python:3.9 /bin/bash -c '

pip install "apache-beam[gcp]"==2.42.0 && \
python -m apache_beam.examples.wordcount --output OUTPUT_FILE && \
HUSTLER=gs://$DEVSHELL_PROJECT_ID-bucket && \
python -m apache_beam.examples.wordcount --project $DEVSHELL_PROJECT_ID \
  --runner DataflowRunner \
  --staging_location $HUSTLER/staging \
  --temp_location $HUSTLER/temp \
  --output $HUSTLER/results/output \
  --region $REGION
'
```

* Go to `Dataflow Jobs` from [here](https://console.cloud.google.com/dataflow/jobs?)

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
