pipeline {
agent any
stages {
stage('Build') {
steps {
sh 'mvn -B -DskipTests clean package'
}
}
stage('K8s') {
steps {
sh 'kubectl set image deployments/hello-node container-name=sismics/ubuntu-jetty:9.4.36
'
}
}
}
}
