pipeline {
	agent any
	tools {
    	maven 'Maven_3_8_1'
	}
	stages {
    	stage("Checkout") {   
        	steps {  
        	    git branch: 'main', url: 'https://github.com/cs680group4/spring-demo.git'
        	}    
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"  
        	}
       	}
   	 
    	stage("Package") {          	 
        	steps {  	 
            	sh "mvn package"  
        	}
       	}
}
}
