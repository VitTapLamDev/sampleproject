@Library('share_Library')
pipeline {
    agent any
    @Library
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
                    if(Files.exists(Paths.get("pipeline2.txt"))){
                        writeFile(file: Files, text: data)
                    } else {
                        FileWriter fw = new FileWriter(file, true);
                    }
                    writeFile(file: "pipeline2.txt", text: "\n" + data)
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