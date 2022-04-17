node('built-in') 
    {
        stage('Continuous Download ') 
         {
            git 'https://github.com/pratiksponde/Maven.git'
         }
        stage('Continuous Build') 
         {
            sh 'mvn package'
         }
	
    }
