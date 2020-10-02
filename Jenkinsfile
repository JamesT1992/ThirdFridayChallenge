pipeline {
	agent Dockerfile
	stages {
		stage(`Create the docker image`){
			steps{
				sudo docker build -t mychallengapp .			
			}
		}
		stage(`Test the app`){
			steps{
				sh "apptest"
			}
		}
		stage(`Push the app to a nexus repository`){
			steps{
				sh "nexuspushtest"
			}
		}
	}
}
