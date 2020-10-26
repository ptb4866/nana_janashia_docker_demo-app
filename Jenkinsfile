pipeline {
    agent none
    stages {
        stage('Select micro services') {
            input {
                message "Select all micro services to deploy?"
                ok "All selected!"
                parameters {
                    choice(name: 'MS1', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS2', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS3', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS4', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                }
            }
            steps {
                echo "Hello, ${params.MS1}. Hello, ${params.MS2}. Hello, ${params.MS3}. Hello, ${params.MS4}"         
            }
        }
        stage('Select single service') {
            input {
                message "Select single micro services to deploy?"
                parameters {
                    choice(name: 'MS5-separate-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'second param with single option')   
                }
            }
            steps {
                echo "Hello, {MS5-separate-param}"         
            }
        }
    }
}