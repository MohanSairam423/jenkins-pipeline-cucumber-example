pipeline{

    agent any

    stages {

        stage ('Compile Stage') {

            steps {
                snDevOpsStep '7dd16550c7173300b8e302b827c260c3'
                withMaven(maven: 'maven_3_5_0') {
                    sh 'mvn clean install'

                }

            }
        }
    stage ('Test Stage') {

            steps {
                snDevOpsStep 'f9d16550c7173300b8e302b827c260c3'
                withMaven(maven: 'maven_3_5_0') {
                    sh 'mvn test'

                }

            }
        }


        stage ('Cucumber Reports') {

            steps {
                snDevOpsStep 'f1d16550c7173300b8e302b827c260c3'
                //cucumber buildStatus: "UNSTABLE",
                //    fileIncludePattern: "**/cucumber.json",
                //    jsonReportDirectory: 'target'

            }

        }

    }

}
