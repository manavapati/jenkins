node { stage('git clone') { 
	
		git branch: 'main', credentialsId: '08da8eb2-1d7f-4ad2-9e75-37670a78f0d7', url: 'https://github.com/manavapati/sep-jai.git'
    }
    stage('Maven clean') {
        sh 'mvn clean'
    }
    stage('Maven validate') {
        sh 'mvn validate'
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
