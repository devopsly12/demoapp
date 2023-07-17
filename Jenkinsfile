def repo = 'https://github.com/devopsly12/demoapp.git'
def branchname = '*/main'

environment 
{
    Maven = tool name: 'Maven_Home'
}
node('windows')
{
stage('checkout')
{
    echo 'demo check out the repositroy'
    echo "$repo"
    checkout scmGit(branches: [[name: "$branchname"]], extensions: [], userRemoteConfigs: [[url: "$repo"]])
}
stage('build')
{
    echo 'build the code $env.BUILD_ID'
    sh 'mvn clean verify'
}
stage('test')
{
   echo 'test the code'
}

}
