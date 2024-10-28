


node('JDK8') {
        stage('SourceCode') {
                git branch: 'sprint1_develop', url: 'https://github.com/dhushyadav/game-of-life.git'
       }

        stage('Build the code') {
                // Maven build process
                sh 'mvn clean package'
       }

        stage('Archiving artifacts & Junit Test Results') {

	archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
	junit stdioRetention: '', testResults: 'gameoflife-web/target/surefire-reports/*.xml'
	}

}
