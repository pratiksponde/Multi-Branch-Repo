node 
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
            sh 'scp /home/ubuntu/.jenkins/workspace/Sample-MultiBranch_master/webapp/target/webapp.war ubuntu@172.31.2.143:/var/lib/tomcat8/webapps/testenv1.war'
         } 
         stage('Continuous Testing') 
         {
            sh 'echo "Test Passed"'
         }
         stage('Continuous Deployment') 
         {
            input message: 'Waiting For Approval ', submitter: 'Admin'
            mail bcc: '', body: 'tuzi aai ghaal madarchod iftaar party khaun haglo aamhi', cc: 'pratikponde12@gmail.com', from: 'patharkar123@gmail.com', replyTo: '', subject: '', to: 'simplynadaf@gmail.com'
            sh 'scp /home/ubuntu/.jenkins/workspace/Sample-MultiBranch_master/webapp/target/webapp.war ubuntu@172.31.2.143:/var/lib/tomcat8/webapps/prodenv1.war'
         } 
    }
