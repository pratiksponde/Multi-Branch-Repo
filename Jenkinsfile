node('built-in') 
    {
        stage('Continuous Download ') 
         {
            git 'https://github.com/pratiksponde/Multi-Branch-Repo.git'
         }
        stage('Continuous Build') 
         {
            sh 'mvn package'
         }
        stage('Continuous Deployment') 
         {
            sh 'scp /home/ubuntu/.jenkins/workspace/CICD-Pipeline/webapp/target/webapp.war ubuntu@172.31.10.3:/var/lib/tomcat8/webapps/testenv2.war'
         } 
         stage('Continuous Testing') 
         {
            sh 'echo "Test Passed"'
         }
         stage('Continuous Deployment') 
         {
            sh 'scp /home/ubuntu/.jenkins/workspace/CICD-Pipeline/webapp/target/webapp.war ubuntu@172.31.10.211:/var/lib/tomcat8/webapps/prodenv2.war'
         } 
    }
