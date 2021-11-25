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
	stage('SonarQube'){	
	sh 'mvn sonar:sonar -Dsonar.host.url=http://34.71.45.99:9000 -Dsonar.login=57eab3e79bc65441f5271a36e3c9b18f3ba0fe65'
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

