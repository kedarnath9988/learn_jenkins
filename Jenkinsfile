pipeline {   
    agent {
        label 'agent-01'
    } //node-01

    options {
        timeout(time:30, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    environment{
        deploy_to = "production"
        GREEATINGS = "hello"
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
      stages {
            stage ("build") {
                steps {
                    sh 'echo this is build'
                }
            }
            stage ("test") {
                steps {
                    sh 'echo this is test'

                }
            }
            stage ("Deploy") {
                steps {
                    sh 'echo this is Deploy'
                }
            }
            stage ("print params"){
                steps {
                    echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"

                echo "trigger test "

                echo "one more trigger "

                echo "2nd one more trigger "

                echo "hello .tst "
                }
            }
        }
        post {
            always(){
                echo "i will run always"
            }

        success(){
            echo " pipeline is successfully compleated"
        }
        failure(){
            echo "pipeline is failure"
        }
        changed(){
            echo " pipe line has changed from the Previously build "
        }
        aborted (){
            echo "pipe line is manually aborted or stoped "
        }
        fixed(){
            echo "currrent pipe-line is successful nut previouslly it is failed "
        }
        }
}