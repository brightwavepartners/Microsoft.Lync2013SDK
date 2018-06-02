pipeline{
  
    agent {
        node {
            label 'master'
            customWorkspace 'a'	
        }
    }

    stages {
        stage('BuildAndTest') {
            steps {
                checkout scm
                bat 'powershell.exe -file ./build.ps1 -Target Default'
            }
        }
    }

    post { 
        always {
            deleteDir()
        }
    }
}