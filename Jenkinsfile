pipeline{
        agent {
            label 'label-01'
        }
        options {
                timeout(time:30, unit:'MINUTES' )
                disableConcurrentBuilds()
                ansiColor('xterm')
        }
        parameters {
            choice(name: 'terraform', choices: ['apply', 'destroy'], description: 'you may apply or destroy the resoureces')
        }
         

        stages {
                stage('int'){
                    steps{
                        sh """

                        cd 01-sg
                        ls -ltr  

                        """
                    }
                }
                stage('plan'){
                        steps{
                            sh """
                                echo thi is test stage
                            """
                        }

                }

                stage('apply'){
                            steps{
                                sh """
                                    echo this is deploy stage 
                                """
                            }
                }

        }

        post {
            always {
                echo 'i will run always and delete the the workspace after the Build '
                deleteDir()
            }
            success {
                echo 'pipeline is successfull'
            }
            failure {
                echo 'pipeline is failed '
            }
        }

}