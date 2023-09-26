@Library('pipeline-library-demo')
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
        stage ('libraries demo'){
            steps {
                echo 'Hello, world'
                sayHello 'Dave'

                echo 'The value of foo is : ' + GlobalVars.foo

                script {
                    def person = new SampleClass()
                    person.age = 21
                    person.increaseAge(10)
                    echo 'Incremented age, is now : ' + person.age
                }
            }
        }
        // stage ('Write'){
        //     steps {
        //         script {
        //             def data = "NguyenDucViet"
        //             if(Files.exists(Paths.get("pipeline2.txt"))){
        //                 writeFile(file: Files, text: data)
        //             } else {
        //                 FileWriter fw = new FileWriter(file, true);
        //             }
        //             writeFile(file: "pipeline2.txt", text: "\n" + data)
        //             sh "pwd"
        //             sh "ls -l"
        //         }
        //     }
        // }
        // stage ('Read'){
        //     steps{
        //         script {
        //             def data = readFile(file: "pipeline2.txt")
        //             println(data)
        //         }
        //     }
        // }
    }
}