pipeline{

    agent any

    stages {

        stage ('Compile Stage') {

            steps {
                snDevOpsStep '7dd16550c7173300b8e302b827c260c3'
                //withMaven(maven: 'maven_3_6_1') {
                    sh 'mvn clean install'
                //}

                

            }
        }
    


        stage ('Cucumber Test Reports') {

            steps {
                snDevOpsStep 'f1d16550c7173300b8e302b827c260c3'
                //sh 'mvn test -Dpublish'
                //cucumber buildStatus: "UNSTABLE",
                  //cucumber  fileIncludePattern: "**/cucumber.json",
                    //jsonReportDirectory: 'target'
                    cucumber '*/.json'
            }

        }

    }

}
