node {
   agent {
      node { label 'slave1' }
   }
    stage('checkout') { 
        git 'https://github.com/praveenkumar1290/Maven-Web-Project.git'
    }
    
    stage('build') {
        bat 'mvn package'
    }
       stage('code-quality') {
        bat 'mvn sonar:sonar -Dsonar.projectKey=guest -Dsonar.host.url=http://localhost:9000 -Dsonar.login=17d0c0b50a0e416b8728c0ba5944169adaa37655'
    }
}
  
