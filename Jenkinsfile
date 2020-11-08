
    pipeline {
    agent none
    stages {
	
 stage('SCM Checkout')
    {
         agent {
                        label "Windows_Node"
                }
        steps {
               git credentialsId: 'f83ee8b5-b4b2-420e-892b-d341e313c937', branch: 'master', url: 'https://github.com/BilelDev/trainingdemo1pipeline.git'
                }
        
    }
	
	stage('BUILD')
    {
         agent {
                        label "Windows_Node"
                }
        steps {
               bat 'build.bat'
                }
        
    }
    	stage('DEPLOY')
    {
         agent {
                        label "Windows_Node"
                }
        steps {
               bat 'deploy.bat'
                }
        
    }
    }
}
