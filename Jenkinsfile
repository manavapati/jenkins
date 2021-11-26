node { stage('git clone') { 
	
		git branch: 'main', credentialsId: '08da8eb2-1d7f-4ad2-9e75-37670a78f0d7', url: 'https://github.com/manavapati/sep-jai.git'
    }
    stage('Maven clean') {
        sh 'maven clean'
    }
    stage('Maven validate') {
        sh 'maven validate'
    }
	stage('Maven test') {
        sh 'maven test'
    }
	stage('Maven package') {
        sh 'maven package'
    }
	stage('Maven deploy') {
        sh 'maven deploy'
    }
}
