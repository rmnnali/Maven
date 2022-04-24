node('built-in')
{
   stage('ContinuousDownload') 
   {
       git 'https://github.com/intelliqittrainings/maven.git'    
   }
   stage('ContinuousBuild')
   {
       sh 'mvn package'
   }
   stage('ContinuousDeployment')
   {
       sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.12.68:/var/lib/tomcat9/webapps/qaapp.war'
   }
   
}
