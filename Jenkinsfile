pipeline {
        agent any
        stages {
                stage('normalstage') {
                        steps {
                                echo 'This is normal stage'
                        }
                }
                stage('Parallelstage') {
                        parallel{
                                stage('parallelstage1') {
                                        steps {
                                                echo 'This is parallelstage 1'
                                        }
                                }
                                stage('parallelstage2') {
                                        steps {
                                                echo 'This is parallelstage 2'
                                        }
                                }
                                stage('parallelstage3') {
                                        steps {
                                                echo 'This is parallelstage 3'
                                        }
                                }
                        }
                }
        }
}
