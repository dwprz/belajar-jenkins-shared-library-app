@Library("belajar-jenkins-shared-library@master") _  // huruf L nya besar

pipeline{

    agent any

    stages{
        stage("Library Resources"){
            steps{
                script{
                    def config = libraryResource("config/build.json")
                    echo config

                }
            }
        }
        stage("Hello Person"){
            steps{
                script{
                  hello.person([
                    "firstName": "Kongleong",
                    "lastName": "Poseidon"
                  ])
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