pipeline {
      stages {
            stage ("build") {
                steps {
                    sh 'echo this is build'
                }
            }
            stage ("test") {
                steps {
                    sh 'echo this is test'
                    sh 'sleep 10'
                }
            }
            stage ("Deploy") {
                steps {
                    sh 'echo this is uDeployat'
                }
            }
        }
}