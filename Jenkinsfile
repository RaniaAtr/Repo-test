pipeline {
    agent any

    stages {
        stage('clon git') {
            steps {
                git branch:'main', url:'https://github.com/RaniaAtr/Repo-test.git'
            }
        }
        stage('Sonarqub') {
            steps{
                 sh ''' 
                 sonar-scanner \
                    -Dsonar.projectKey=test-front-rania \
                    -Dsonar.sources=. \
                    -Dsonar.host.url=https://2a26-212-114-26-208.ngrok-free.app \
                    -Dsonar.token=sqp_09c4b879899c5ab57654e00021ae6aa162e1f002
                    '''


            }
        }
    }
}