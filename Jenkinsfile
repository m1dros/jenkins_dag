pipeline {
    agent any
    parameters {
        choice(name: 'Script', choices: ['All', 'python', 'Bash', 'C.script'], description: 'Choice Script')
    }
    stages {
        stage('Script python') {
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'python' }
                }
            }
            steps {
                sh 'cat python'
            }
        }
        stage('Script Bash') {
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'Bash' }
                }
            }
            steps {
                sh 'cat Bash'
            }
        }
        stage('Script C') {
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'C' }
                }
            }
            steps {
                sh 'cat C'
            }
        }
    }
}
