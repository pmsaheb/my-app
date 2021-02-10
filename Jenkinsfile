node {
    stage ('SCM Checkout') {
        git 'https://github.com/pmsaheb/my-app.git'
    }
    stage ('Compile and Package') {
        def mvnHome = tool name: 'Maven1', type: 'maven'
        sh "${mvnHome}/bin/mvn clean package" 
    }
}
