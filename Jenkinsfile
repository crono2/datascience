node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t datascience:express2 ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'crono2' -p 'devops@2019' "
sh "docker tag datascience:express2 crono2/datascience:express2"
sh "docker push crono2/datascience:express2"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}