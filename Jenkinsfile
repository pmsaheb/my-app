node {
    stage ('SCM Checkout') {
        git 'https://github.com/pmsaheb/my-app.git'
    }
    stage ('Compile and Package') {
        mvnHome = /opt/apache-maven-3.6.3
        sh "${mvnHome}/bin/mvn clean package" 
    }
}
