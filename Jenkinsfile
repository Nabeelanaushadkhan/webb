pipeline{
agent any
tool{
maven 'MyMaven'
}
stages{
stage('Checkout'){
steps{
git branch: 'main', url: 'https://github.com/Nabeelanaushadkhan/webb.git'
}
}
stage('Build'){
steps{
sh 'mvn clean package'
}
}
stage('Archive Artifacts'){
steps{
archiveArtifacts artifacts: 'target/*.war'
}
}
stage('Deploy'){
steps{
sh 'mvn clean package'
}
}
}
post{
success{
echo'Success'
}
failure{
echo'fail'
}
}
}
