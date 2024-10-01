pipeline {
    agent  {
        label 'Agent-01'
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