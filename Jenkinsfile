node {
    stage ('SCM Checkout') {
        git 'https://github.com/pmsaheb/my-app.git'
    }
    stage ('Compile and Package') {
        def mvnHome = tool name: 'Maven1', type: 'maven'
        sh "${mvnHome}/bin/mvn clean package" 
    }
    stage ('deploy to tomcat') {
        sshagent(['tomcat-demo']) {
        sh 'scp -o StrictHostKeyChecking=no target/*.war ubuntu@<ip address>:/opt/tomcat9/webapps/'
        }
    }
}
