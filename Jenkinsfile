node {
   stage('SCM Checkout'){
	git 'https://github.com/NikitaBr-503/kanban-war.git'
   }

   stage('Mvn Build'){
	   // Build using maven
	   def mvnHome = tool name: 'maven3', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }

   stage('deploy to tomcat'){
      sshagent(['tomcat-dev']) {
	      sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@3.87.143.19:/usr/share/tomcat8/webapps/'
      }
   }

}