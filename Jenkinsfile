pipeline{
        agent {
            label 'node-01'
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
                stage('Build'){
                    steps{
                        sh """
                        ls -ltr 
                        """
                    }
                }
                stage('test'){
                        steps{
                            sh """
                                echo thi is test stage
                            """
                        }

                }

                stage('deploy'){
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