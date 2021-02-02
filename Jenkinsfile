pipeline
{
	agent any
	stages{
		stage('Build Application'){
		steps{
		bat 'mvn clean install'
		}
		}
		stage('Deploy Application to MuleSoft CloudHub'){
		steps{
		bat 'mvn package deploy -DmuleDeploy'
		}
		}
		stage('Perform Regression Testing'){
		steps{
		newman run C:\\Users\\Camerina\\Documents\\newman\\MorelosTimeZone.postman_collection.json --disable-unicode
		}
		}
	}
}