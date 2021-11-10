pipeline {
   agent any

   stages {
   
      stage('Pull Source Code') {
          steps {
              git credentialsId: 'dimalife', branch: 'master' , url: 'https://github.com/DimaLife/simple-java-maven-app.git'
          }
      }
      
      stage('deploy to kubesphere') {
          steps {
            kubernetesDeploy(enableConfigSubstitution: false, kubeconfigId: 'gke', configs: 'app.yaml')
          }
      }
   }
}
