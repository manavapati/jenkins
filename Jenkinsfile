node { stage('git clone') { 
	
		git branch: 'main', credentialsId: '08da8eb2-1d7f-4ad2-9e75-37670a78f0d7', url: 'https://github.com/manavapati/sep-jai.git'
    }
    stage('Maven clean') {
        sh 'mvn clean'
    }
    stage('Maven validate') {
        sh 'mvn validate'
    }
	stage('SonarQube'){	
	sh 'mvn sonar:sonar -Dsonar.host.url=http://34.125.73.121:9000 -Dsonar.login=5f52606c7ceff14f29167af154fd7da5065ed44e'
	}
	stage('Maven test') {
        sh 'mvn test'
    }
	stage('Maven package') {
        sh 'mvn package'
    }
	stage('Maven deploy') {
        sh 'mvn deploy'
    }
}
