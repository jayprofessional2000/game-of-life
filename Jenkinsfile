node {
  stage('scm') {
    git 'https://github.com/jayprofessional2000/game-of-life.git'
  }
  stage('buold and package') {
    sh 'mvn package'
  }
  stage('results') {
    archive 'gameoflife-web/target/gameoflife.war'
	junit 'gameoflife-web/target/surefire-reports/*.xml'
  }
}
