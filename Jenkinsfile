node {
	stage('cloning git repo'){
	git credentialsId: 'dfb0c209-273e-47ee-b76a-b88ab7eec3dc', url: 'https://github.com/riteshmca10/repo2.git'
	sh label: '', script: '''cd /var/tmp/
	rm -rf repo2
	git clone https://github.com/riteshmca10/repo2.git
	cd repo2
	ls -al'''
	}
	
	stage('mail notification') {
	mail from: "jenkinstesting@gmail.com",
	to: "was.riteshkumar82@gmail.com",
	subject: "ansible deployement status" ,
	body: "jenkins job ${env.JOB_NAME} - build ${env.BUILD_NUMBER} ${currentBuild.currentResult} ${env.JOB_URL} complete"
	}
	

}
