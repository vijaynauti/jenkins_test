pipeline {
        agent any
        stages {
                stage('stage1') {
                        steps {
                                echo 'This is normal stage'
                        }
                }
        }
        post {
                failure {
                        echo 'This is post build step'
                }
        }
}
