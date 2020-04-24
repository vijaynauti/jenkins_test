pipeline {
        agent any
        parameters {
                string( name: 'NAME', defaultValue: 'jenkinstraining', description: 'please enter your name')
                text( name: 'BIO', defaultValue: '', description: 'please say something about you')
                choice( name: 'CHOICE', choices:  ['one', 'two', 'three'], description: 'please chose one')
                booleanParam( name: 'BOOLEAN', defaultValue: true, description: 'please select boolean value')
                password( name: 'PASSWORD', defaultValue: 'test123', description: 'please enter password')
        }
        stages {
                stage('print values') {
                        steps {
                                echo "Hello ${params.NAME}"
                                echo "Your Biography: ${params.BIO}"
                                echo "Your choice is: ${params.CHOICE}"
                                echo "Your boolean choice is: ${params.BOOLEAN}"
                                echo "your password is: ${params.PASSWORD}"
                        }
                }
        }
}
