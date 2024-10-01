pipeline {
    agent  {
        label 'Agent-01'
    } 
    options {
        timeout (time: 1, units:'SECONDS')
    }
        stages {
            stage ("dev") {
                steps {
                    sh 'echo this is dev'
                }
            }
            stage ("qa") {
                steps {
                    sh 'echo this is qa'
                    sh 'sleep 10'
                }
            }
            stage ("uat") {
                steps {
                    sh 'echo this is uat'
                }
            }
            stage ("prod") {
                steps {
                  sh 'echo this is prod'  
                }
            }


        }
}