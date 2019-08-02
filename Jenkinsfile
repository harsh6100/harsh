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
	  
	  
	    bat '''copy C:\\Program Files (x86)\\Jenkins\\workspace\\pipe-autodeploy1\\target\\*.war C:\\Program Files\\Apache Software Foundation\\Tomcat 7.0_Tomcat8\\webapps'''
   }
}
