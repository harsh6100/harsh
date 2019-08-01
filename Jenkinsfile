ode {

   def mvn = tool (name: 'maven', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    
	git branch: 'master',	
	url: 'https://github.com/javahometech/myweb'
   
   }
     
	
   stage('Compile and build'){
	  
	   
	   sh "${mvn} package"
   }
}
