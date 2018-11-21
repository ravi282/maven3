
node('loan') 
{
    stage('ContinuousDownload-loan') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'

    }
    stage('ContinuousBuild-loan') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment-loan')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/multibranch/webapp/target/webapp.war ubuntu@172.31.22.28:/var/lib/tomcat7/webapps/qaenv.war'
    }
    stage('Continuoustesting-loan')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    
    
 
    
    
    
}

