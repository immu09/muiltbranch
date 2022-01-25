node('built-in') 
{
    stage('Continuous Download_Master') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_Master') 
	{
    sh label: '', script: 'mvn package'
	}
	 stage('Continus Build')
		    {
         sh 'scp  /home/ubuntu/.jenkins/workspace/multibranch_project_master/webapp/target/webapp.war   ubuntu@172.31.36.152:/var/lib/tomcat8/webapps/qqai.war'

           }
    }
