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
                always {
                        echo 'This is post build step'
                }
        }
}
