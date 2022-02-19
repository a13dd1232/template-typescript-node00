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

### Transfer files using the Google Cloud CLI - Local Machine -> Cloud Shell:

*** (Copy a file, data.txt, from Local Machine to your Cloud Shell) ***

*** Must***
gcloud cloud-shell ssh
*** Must***

### Transfer files using the Google Cloud CLI - Cloud Shell -> Local Machine:

*** (Copy a file, data.txt, from Cloud Shell to your local machine) ***

*** Must***
gcloud cloud-shell ssh
*** Must***



gcloud cloud-shell scp cloudshell:\/data.txt localhost:\data.txt

echo "# Test File" >> TestFile.md

gcloud cloud-shell scp localhost:\TestFile.md cloudshell:\/TestFile.md

gcloud cloud-shell scp localhost:\/workspace/template-typescript-node00/gcloud/TestFile.md cloudshell:\/TestFile.md 

gcloud cloud-shell scp localhost:\/ cloudshell:\ 
gcloud cloud-shell scp localhost:\/workspace/template-typescript-node00/gcloud/CloudShell/Test.md cloudshell:\/home/student_01_bcd38ba2aaa9/Test.md
/workspace/template-typescript-node00/gcloud/CloudShell/Test.md
/home/student_01_bcd38ba2aaa9/Test.md


## Transfer files using the Google Cloud CLI - Local Machine -> Compute Engine (Virtual Machine (VM) Instance):

*** Must***
gcloud compute ssh --zone "us-central1-f" "gcelab"  --project "qwiklabs-gcp-04-461a4ecff612"
gcloud compute ssh "gcelab"

For Apache2 Folder:
sudo chown -R $USER /var/www

For Nginx Folder:
sudo chown -R $USER /usr/share/nginx/html


*** Must***


gcloud compute scp LOCAL_FILE_PATH VM_NAME:~

gcelab:

/var/www/html

/workspace/template-typescript-node00/gcloud/html

/var/www/

gcloud compute scp LOCAL_FILE_PATH VM_NAME:~

gcloud compute scp --recurse /workspace/template-typescript-node00/gcloud/html root@gcelab:/var/www/

## Transfer files using the Google Cloud CLI - Compute Engine (Virtual Machine (VM) Instance) -> Local Machine:


### mount Cloud Shell home directory onto local file system:

If you're using Mac or Linux, you can mount your Cloud Shell home directory onto your local file system after installing sshfs.

This allows you to edit the files in your Cloud Shell home directory using your choice of local tools. All the data in your remotely mounted file system is stored on a Persistent Disk and stored across sessions.


gcloud cloud-shell get-mount-command /workspace/template-typescript-node00/gcloud

/workspace/template-typescript-node00/gcloud


/workspace/template-typescript-node00/gcloud/CloudShell

/home/student_01_fa76baf72943

gcloud alpha cloud-shell get-mount-command /workspace/template-typescript-node00/gcloud/CloudShell


