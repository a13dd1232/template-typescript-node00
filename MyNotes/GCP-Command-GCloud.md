# GCP-Command-GCloud.md

## Install GCloud Command:

sudo apt-get -y install apt-transport-https ca-certificates gnupg

echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -

sudo apt-get update && sudo apt-get install google-cloud-sdk

gcloud init

## Using Cloud Shell with the gcloud CLI:

https://cloud.google.com/shell/docs/using-cloud-shell-with-gcloud-cli

### Start a SSH session:

gcloud cloud-shell ssh

### Copy a file, data.txt, from Cloud Shell to your local machine:

gcloud cloud-shell scp cloudshell:\/data.txt localhost:\data.txt

### mount Cloud Shell home directory onto local file system:

If you're using Mac or Linux, you can mount your Cloud Shell home directory onto your local file system after installing sshfs.

This allows you to edit the files in your Cloud Shell home directory using your choice of local tools. All the data in your remotely mounted file system is stored on a Persistent Disk and stored across sessions.


gcloud cloud-shell get-mount-command /workspace/template-typescript-node00/gcloud

/workspace/template-typescript-node00/gcloud

