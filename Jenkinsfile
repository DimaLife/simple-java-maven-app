pipeline {
   agent any

   stages {
   
      stage('Pull Source Code') {
          steps {
              git branch: 'danushkevich' , url: 'git@github.com:MNT-Lab/helloworld-project.git'
          }
      }
      
      stage('deploy to kubesphere') {
          steps {
            kubernetesDeploy(enableConfigSubstitution: false, kubeconfigId: 'gke', configs: 'app.yaml')
          }
      }
   }
}
