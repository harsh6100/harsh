node {

   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    
	git branch: 'master',	
	url: 'https://github.com/harsh6100/harsh'
   
   }
     
	stage('Compile'){
	  
	   
	   bat "${mvn} compile"
   }
   stage('Build'){
	  
	   
	   bat "${mvn} package"
   }
  stage('Test'){
	  
	  
	  bat "${mvn} test"
   }
	
	stage('Deploy'){
	  
	  
		deploy adapters: [tomcat7(credentialsId: 'manager', url: 'http://localhost:8083')], contextPath: 'project', war: 'target/*.war'
   }
}
