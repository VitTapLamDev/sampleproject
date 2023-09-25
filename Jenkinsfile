pipeline {
    agent any
    
    stages {
        stage ('Display'){
            steps {
                script {
                    echo "pipeline2"
                }
            }
        }
        stage ('Write'){
            steps {
                script {
                    def data = "NguyenDucViet"
                    writeFile(file: "pipeline2.txt", text: data)
                    sh "pwd"
                    sh "ls -l"
                }
            }
        }
        stage ('Read'){
            steps{
                script {
                    def data = readFile(file: "pipeline2.txt")
                    println(data)
                }
            }
        }
    }
}