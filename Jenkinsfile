node {
   //def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	//git branch: 'master',
	//credentialsId: 'github',
	url: 'https://github.com/NikitaBr-503/kanban-war.git'
   }

   stage('Mvn Build'){
	   // Build using maven
	   def mvnHome = tool name: 'maven3', type: 'maven'
	   sh "${mvnHome}/bin/mvn package"
   }

}