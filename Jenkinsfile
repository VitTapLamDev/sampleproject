pipeline {
    agent any
    
    stages {
        stage ('Run Python Script') {
            steps {
                sh "python script.py --paht ${params.demo_path} --user ${params.demo_user}"
            }
        } 
    }
}