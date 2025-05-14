pipeline{
	any agent
		tools{
			maven 'Maven'
		}
		stages{
			stage('Checkout'){
				steps{
					git branch:'master', url:''
					}
				}
			stage('Build'){
				steps{
					sh 'mvn clean package'
					}
				}
			stage('Test'){
				steps{
					sh 'mvn test'
					}
				}
			stage('Run Application'){
				steps{
					sh 'java -jar target/'
					}
				}
			}
}
