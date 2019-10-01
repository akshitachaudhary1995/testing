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
               
                              steps {
                                echo("Running the integration test...")
                              }
                           }
                           }
                           }
              
