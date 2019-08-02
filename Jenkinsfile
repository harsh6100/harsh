node {

   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    
	git branch: 'master',	
	url: 'https://github.com/harsh6100/harsh'
   
   }
     
	
   stage('Compile and build'){
	  
	   
	   bat "${mvn} package"
   }
  stage('Test'){
	  
	  
	  bat "${mvn} test"
   }
	
	stage('Deploy'){
	  
	  
		deploy adapters: [tomcat7(credentialsId: 'manager', url: 'http://localhost:8083')], contextPath: 'deploy', war: 'target/*.war'
   }
}
