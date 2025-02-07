pipeline {   
    agent {
         label 'Agent-01'
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
        }
}