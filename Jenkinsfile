node {
    
    properties([[$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '5', numToKeepStr: '5']]]);
    
    //def mvnHome = tool 'Maven350'
    
    stage ('Checkout from GIT') {    
      git url: 'https://github.com/MuraliYarramsetti/gameoflife.git'
    }
    
    stage ('Maven Build') {    
      def mvnHome = tool 'Maven350'
      sh "${mvnHome}/bin/mvn clean install -DskipTests=true"
    } 
}
