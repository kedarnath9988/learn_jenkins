pipeline {   
    agent {
        label 'agent-01'
    } //node-01
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
        }
}