pipeline {

  agent { label 'kubepod' } 

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/seshumdevops/kubernetessetup.git' , branch:'test'
      }
    }

    stage('Deploy APP') {
      steps {
         script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

 }
}
