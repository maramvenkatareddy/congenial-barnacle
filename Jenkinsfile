pipeline {
    agent any
    environment {
        url = 'https://github.com/maramvenkatareddy/spring-petclinic.git'
    }
    stages {
        stage('SCM'){
            steps{
                git url: "${params.URL}", 
                    branch: 'main'
            }
        }
        stage ('build') {
            when {
                    branch 'main'
                    environment(name: "url", value: "https://github.com/maramvenkatareddy/spring-petclinic.git")
                  }
            steps {
                sh 'mvn package'
            }
        }
    }
}
