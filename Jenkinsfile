node {
    stage ('SCM Checkout') {
        git 'https://github.com/pmsaheb/my-app.git'
    }
    stage ('Compile and Package') {
        sh 'mvn clean package' 
    }
}
