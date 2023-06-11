pipeline {
    agent any
       environment {
        SAMPLE_GLOBAL_ENV_VAR = "C:/Users/Raza Ahmed/Desktop/FST Training Tool/jenkins_workshop"
       // SAMPLE_ENV = credentials("simple-secret-text")
       // MYUSERPASS = credentials("test-user-pass")
    }

    parameters {
        booleanParam(name: "TEST_BOOLEAN", defaultValue: true, description: "Sample boolean parameter")
        string(name: "TEST_STRING", defaultValue: "JenkinsWorkshop", trim: true, description: "Sample string parameter")
        text(name: "TEST_TEXT", defaultValue: "Jenkins Pipeline Tutorial", description: "Sample multi-line text parameter")
        password(name: "TEST_PASSWORD", defaultValue: "SECRET", description: "Sample password parameter")
        choice(name: "TEST_CHOICE", choices: ["production", "staging", "development"], description: "Sample multi-choice parameter")
    }
    
    stages {
        stage('Create Directory') {
            steps {
              bat '''cd C:\\Users\\Raza Ahmed\\Desktop\\FST Training Tool\\jenkins_workshop
              mkdir demoFolder2'''
                echo 'Create Diectory'
            }
             post {
                always {
                    echo "Create Directory Using Combined Pipeline."
                }
            }
        }
        stage('Create File') {
            steps {
            bat '''cd C:\\Users\\Raza Ahmed\\Desktop\\FST Training Tool\\jenkins_workshop\\demoFolder2
            copy nul > file.txt'''
                echo 'Create File'
            }
            post {
                always {
                    echo "Create File Using Combined Pipeline."
                }
            }
        }
        stage('Write Content in File') {
            steps {
                bat '''cd C:\\Users\\Raza Ahmed\\Desktop\\FST Training Tool\\jenkins_workshop\\demoFolder2
                echo This is a test> file.txt
                '''
                echo 'Write Content in File'
            }
             post {
                always {
                    echo "Write Content in File Using Combined Pipeline."
                }
            }
        }
    }
}
