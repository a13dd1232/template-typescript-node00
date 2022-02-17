# GCP-Setup-Commands

qwiklabs-gcp-01-711ff6eabe57

# 00.- gcloud CLI

gcloud -h

gcloud config --help

gcloud help config




${GOOGLE_CLOUD_PROJECT}
echo ${GOOGLE_CLOUD_PROJECT}
GOOGLE_CLOUD_PROJECT=''

export GOOGLE_CLOUD_PROJECT=<your_project_ID>
export PROJECT_ID=<your_project_ID>
export REGION=<your_region>
export ZONE=<your_zone>

gcloud config set compute/region <REGION>
gcloud config set compute/zone <ZONE>

gcloud auth list

gcloud config list

gcloud config list --all

gcloud config list project

gcloud components list

gcloud compute project-info describe --project <your_project_ID>

export GOOGLE_CLOUD_PROJECT=qwiklabs-gcp-01-711ff6eabe57
export PROJECT_ID=qwiklabs-gcp-01-711ff6eabe57
export ZONE=us-central1-a
export REGION=us-central1

echo $GOOGLE_CLOUD_PROJECT
echo $PROJECT_ID
echo $ZONE
echo $REGION

gcloud config set compute/region $REGION
gcloud config set compute/zone $ZONE

gcloud config get-value compute/zone
gcloud config get-value compute/region

gcloud compute project-info describe --project ${GOOGLE_CLOUD_PROJECT}

gcloud compute instances create gcelab --machine-type n1-standard-2 --zone $ZONE --tags http-server

gcloud compute instances create gcelab2 --machine-type n1-standard-2 --zone $ZONE --tags http-server

gcloud compute instances create gcelab3 --machine-type n1-standard-2 --zone $ZONE --tags http-server

gcloud compute ssh gcelab2 --zone $ZONE







zzz