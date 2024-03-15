pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mymaven"
        jdk "myjava"
    }

    stages {
        stage('Compile') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/edureka-git/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                bat "mvn compile"

                // To run Maven on a Windows agent, use
                // bat "mvn complie"
            }
        }
        stage('CodeReview') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/edureka-git/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                bat "mvn pmd:pmd"

                // To run Maven on a Windows agent, use
                // bat "mvn complie"
            }
        }
        stage('Unit Test') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/edureka-git/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                bat "mvn test"

                // To run Maven on a Windows agent, use
                // bat "mvn complie"
            }
        }
        stage('QA Matrix') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/edureka-git/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                bat "mvn cobertura:cobertura -Dcobertura.report.format=xml"

                // To run Maven on a Windows agent, use
                // bat "mvn complie"
            }
        }
        stage('Package') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/edureka-git/DevOpsClassCodes.git'

                // Run Maven on a Unix agent.
                bat "mvn package"

                // To run Maven on a Windows agent, use
                // bat "mvn complie"
            }
        }
    }
}
