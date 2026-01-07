pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    credentialsId: 'ghp_qSyqyDd051Ty7evhmNHYvNY9DNXasy4GduR',
                    url: 'https://github.com/ChilakalaThouheed/9am-devops.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Build started'
            }
        }
    }
}
