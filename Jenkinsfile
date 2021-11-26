node {
       stage('git clone') {
        git credentialsId: '1d29b97f-bc55-4634-9022-4b50dfb50a45', url: 'https://github.com/ksproapp/ks.git'
    }
	stage('Maven Clean') {
        sh 'mvn clean'
    }
	stage('Maven validate') {
        sh 'mvn validate'
    }
	
	stage('Maven Test') {
        sh 'mvn test'
    }
	stage('Maven Package') {
        sh 'mvn package'
    }
	stage('Maven Deploy') {
        sh 'mvn deploy'
    }
}

