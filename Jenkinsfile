
    
node {
    
   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
    
        stage('compile stage') {
         
                sh "${mvn} compile"
            
           
        }
        stage('test') {
        
                 sh "${mvn} test"
            
           
        }
    }




