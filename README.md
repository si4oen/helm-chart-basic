
**Helmchart Installation Guilde**

*Install Helm (Centos)*
  - wget https://get.helm.sh/helm-v3.3.2-linux-amd64.tar.gz or select desire version here https://github.com/helm/helm/releases
  - tar -zxvf helm-v3.3.2-linux-amd64.tar.gz
  - sudo mv linux-amd64/helm /usr/local/bin/helm


*Create Helm Chart*
  - helm create your-chart-name


*Index Helm Repo*
  - helm package your-chart-name
  - mkdir helm-repo
  - mv your-chart-name-0.1.0.tgz helm-repo/
  - helm repo index helm-repo --url https://helm-repo.your-domain
  - upload file .tgz and index.yaml to bucket s3


*How To Use*
  - helm repo add helm-repo https://helm-repo.your-domain
  - touch values.yml
  - helm template <service-name> helm-repo/your-chart-name -f values.yaml




