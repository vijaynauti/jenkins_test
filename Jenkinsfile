pipeline {
        agent any
        options {
                timestamps()
                ansiColor("xterm")
        }
        stages {
                stage("step1") {
                        options {
                                timeout(time: 1, unit: "MINUTES")
                        }
                        steps {
                                sh 'printf "\\e[31mexecuting step1\\e[0m\\n"'
                        }
                }
                stage("step2") {
                        when {
                                environment name: "state", value: "test"
                        }
                        options {
                                timeout(time: 2, unit: "MINUTES")
                        }
                        steps {
                                sh 'printf "\\e[31mexecuting step2\\e[0m\\n"'
                        }
                }
        }
}
