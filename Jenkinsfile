pipeline {
         agent any
         stages {
                 stage('One') {
                 steps {
                     echo('Heyaaa.....This is Akshuzz Cool Pipeline')
                 }
                 }
                 stage('Two') {
                 steps {
                    input('Do you want to have some fun in the pipeline?')
                 }
                 }
                 stage('Three') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                 steps {
                       echo("Hello")
                 }
                 }
                 stage('Four') {
                 parallel { 
                            stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                            stage('Integration test') {
                              agent {
                                    docker {
                                            reuseNode true
                                            image 'ubuntu'
                                           }
                                    }
                              steps {
                                echo("Running the integration test...")
                              }
                           }
                           }
                           }
              }
}
