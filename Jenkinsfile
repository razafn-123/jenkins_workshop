pipeline {
    agent any
    //agent none -- is used to disable global agent for the entire pipeline
    // agent { label "linux" } -- is used to execute the whole pipeline or a specific stage on a node with a specific label
    // agent { docker "alpine"} -- is used to execute the entire pipeline or a specific stage inside a docker container
    // agent { dockerfile true } --Docker related directive that is used to build a docker image from an existing Dockerfile
    stages {
        stage("Build") {
            // agent any -- execute the pipeline or a specific stage on any available agent
            steps {
                echo "Build stage."
            }
        }
        stage("Test") {
            // agent any
            steps {
                echo "Test stage."
            }
        }
        stage("Release") {
            // agent any
            steps {
                echo "Release stage."
            }
        }
    }
}