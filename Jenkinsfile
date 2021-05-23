node {
    stage('scm'){
        git 'https://github.com/jayprofessional2000/game-of-life.git'
    }
    stage('building'){
        sh 'mvn clean package'
    }
    stage('Archiving'){
        archive 'gameoflife-web/target/gameoflife.war'
    }
    stage('junit'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}