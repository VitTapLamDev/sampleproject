@Library('pipeline-library-demo') _
import com.cleverbuilder.GlobalVars
import com.cleverbuilder.SampleClass

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
                script {
                    log.info 'Started !'

                    echo 'Hello, world'
                    

                    echo 'The value of foo is : ' + GlobalVars.foo
                    def person = new SampleClass()
                    person.name = 'Viet Nguyen'
                    sayHello person.name
                    person.age = 21
                    person.increaseAge(10)
                    echo person.name + 'next year is ' + person.age + 'years old'
                    echo 'Incremented age, is now : ' + person.age

                    log.warning 'Finished!'
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