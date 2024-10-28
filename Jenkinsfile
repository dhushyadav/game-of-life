pipeline{

	agent { label 'JDK8'}

	stages{

		stage('checkout the code'){

			steps {
	
				git branch: 'sprint1_develop', url: 'https://github.com/dhushyadav/game-of-life.git'


			}
		}
		stage('build th code'){

			steps{
				 sh 'mvn clean package'
				}
				
			}

		stage('artifacts and test'){

		steps{
			archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
			junit stdioRetention: '', testResults: 'gameoflife-web/target/surefire-reports/*.xml'
				}
			}


	}

}
