
find / -type f -exec grep -H 'text-to-find-here' {} \;

find . -name 'Dockerfile*'  -exec cp {} ./workspace/template-typescript-node00/DockerFilesList1 \;

find . -name 'Dockerfile*'  -exec grep -H 'mongo*' {}  \;



