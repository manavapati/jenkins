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
	sh 'mvn sonar:sonar -Dsonar.host.url=http://34.125.200.25:9000 -Dsonar.login=a6523fe185f46a699a25ce663d5a84d16ed50fd8'
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
