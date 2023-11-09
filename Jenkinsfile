@Library("belajar-jenkins-shared-library@master") _  // huruf L nya besar

pipeline{

    agent any

    stages{
        stage("Maven Compile"){
            steps{
                script{
                  maven(["clean", "compile", "test"])
                }
            }
        }
        stage("Hello World"){
            steps{
                script{
                  hello.world() // hello.hello() artinya memanggil file hello.groovy dan function world() di repository belajar-jenkins-shared-library
                }
            }
        }
        stage("Global Variable") {
            steps{
                script{
                    echo(author())
                    echo(author.name())
                    echo(author.title())
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