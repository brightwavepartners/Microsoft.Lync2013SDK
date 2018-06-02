pipeline{
  
    agent {
        node {
            label 'master'
            customWorkspace 'a'	
        }
    }

    stages {
        stage('PackageAndPublish') {
            steps {
                checkout scm
                bat 'nuget.exe'
            }
        }
    }

    post { 
        always {
            deleteDir()
        }
    }
}