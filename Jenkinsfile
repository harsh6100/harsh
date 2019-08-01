
    
node {
    
   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
    stages {
        stage('compile stage') {
            steps {
                sh "${mvn} compile"
            }
           
        }
        stage('test') {
            steps {
                 sh "${mvn} test"
            }
           
        }
    }
}



