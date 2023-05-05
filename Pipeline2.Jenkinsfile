pipeline {
    agent any
    stages {
        stage ('Build') {
            try {
                agent {
                    docker {
                        image 'gradle:6.7-jdk11'
                        // Run the container on the node specified at the
                        // top-level of the Pipeline, in the same workspace,
                        // rather than on a new node entirely:
                        reuseNode true
                    }
                }
                steps {
                    sh 'gradle --version'
                }
            }
            catch (e) {
                currentBuild.result = "FAILED"
                throw e
            }
            finally {
                mail to:"os.olaniyi@outlook.com",
                    subject: "STATUS FOR PROJECT: ${currentBuild.fullDisplayName}",
                    body: "RESULT: ${currentBuild.result}"
            }
        }
    }
}