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
                echo "Hello, ${MS1-param}. Hello, ${MS2-param}. Hello, ${MS3-param}. Hello, ${MS4$-param}"         
            }
        }
        stage('Select single service') {
            input {
                parameters [
                    choice(name: 'MS5-separate-param', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'second param with single option')   
                ]
            }
            steps {
                echo "Hello, ${MS5-separate-param}"         
            }
        }
    }
}