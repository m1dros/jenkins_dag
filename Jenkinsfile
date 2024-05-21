pipeline {
    agent any
    parameters {
        choice(name: 'Script', choices: ['All', 'python', 'Bash', 'C.script'], description: 'Choice Script' )
    }
    stages {
        stage('Script python') {
            steps {
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'python' }
                    }
                }
            }
        }
        stage('Script Bash'){
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'Bash' }
                }
            }
        }
        stage('Script C') {
            when {
                anyOf {
                    expression { params.Script == 'All' }
                    expression { params.Script == 'C' }
                }
            }
        }
    }
}
