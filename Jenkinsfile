pipeline {
  agent any
  stages {
  stage( "Build" ){
    steps {
    echo "running build stage"
    sh "./gradlew build --no-daemon"
    }
    
  }

  stage("Archive Artifact"){
    steps {
    echo "Archiving Artifacts"
    archiveArtifacts artifacts: 'dist/trainSchedule.zip', onlyIfSuccessful: true
    }
  }
  
}

}
