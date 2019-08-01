node {

   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    
	git branch: 'master',	
	url: 'https://github.com/harsh6100/harsh'
   
   }
     
	
   stage('Compile and build'){
	  
	   
	   sh "${mvn} package"
   }
}
