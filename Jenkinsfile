pipeline {
    agent none
    stages {
        stage('Select micro services') {
            input {
                message "Select all micro services to deploy?"
                ok "All selected!"
                parameters {
                    choice(name: 'MS1-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS2-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS3-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                    choice(name: 'MS4-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'input ms')
                }
            }
            steps {
                echo "Hello, ${params.MS1-param}. Hello, ${params.MS2-param}. Hello, ${params.MS3-param}. Hello, ${params.MS4$-param}"         
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
                echo "Hello, $params.{MS5-separate-param}"         
            }
        }
    }
}