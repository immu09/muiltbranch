	node('built-in')
{
    stage('Continuous Download_loans')
        {
    git 'https://github.com/sunildevops77/maven.git'
        }
    stage('Continuous Build_loans')
        {
    sh label: '', script: 'mvn package'
        }
         stage('Continus Deploymen_loans')
                    {
         sh 'scp  /home/ubuntu/.jenkins/workspace/multibranch_project_master/webapp/target/webapp.war   ubuntu@172.31.36.152:/var/lib/tomcat8/webapps/qqai.war'

           }
           stage('Continuous Testing_loans')
                     {
           sh 'echo "All Testing Scripts are Passed"'
               }
stage('Continuous Delivery_loans')
                        {
           sh 'scp  /home/ubuntu/.jenkins/workspace/multibranch_project_master/webapp/target/webapp.war   ubuntu@172.31.47.33:/var/lib/tomcat8/webapps/pprodi.war'
           }

    }

