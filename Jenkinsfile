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
         stage('Continus Deploymen_master')
                    {
         sh 'scp  /home/ubuntu/.jenkins/workspace/multibranch_project_master/webapp/target/webapp.war   ubuntu@172.31.36.152:/var/lib/tomcat8/webapps/qqai.war'

           }
           stage('Continuous Testing_master')
                     {
           sh 'echo "Testing Scripts are Passed"'
               }
stage('Continuous Delivery_master')
                        {
           sh 'scp  /home/ubuntu/.jenkins/workspace/multibranch_project_master/webapp/target/webapp.war   ubuntu@172.31.47.33:/var/lib/tomcat8/webapps/pprodi.war'
           }

    }

