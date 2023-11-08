@library("belajar-jenkins-shared-library@master")

pipeline{

    agent any

    stages{
        stage("Hello World"){
            steps{
                script{
                  hello.hello() // hello.hello() artinya memanggil file hello.groovy dan function hello() di repository belajar-jenkins-shared-library
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}