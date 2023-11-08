@Library("belajar-jenkins-shared-library@master") _

pipeline{

    agent any

    stages{
        stage("Hello World"){
            steps{
                script{
                  hello.world() // hello.hello() artinya memanggil file hello.groovy dan function world() di repository belajar-jenkins-shared-library
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