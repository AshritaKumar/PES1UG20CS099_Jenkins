pipeline {
agent any

stages {
stage('Build') {
steps {
sh 'g++ -o hello working.cpp'
}
}

stage('Test') {
steps {
sh './hello'
}
}

stage('Deploy') {
steps {
echo 'deployed successfully'
}
}
}

post {
always {
script {
if (currentBuild.result == 'FAILURE') {
echo 'pipeline failed'
}
}
}
}
}
