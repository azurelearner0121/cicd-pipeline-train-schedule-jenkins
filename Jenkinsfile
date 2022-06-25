pipeline {
  agent { label "dev-agent"}
  stages { 
    stage('Build') {
      steps {
        echo 'RunningBuildStage'
        sh('./gradlew build --no-daemon')
        
      }
    }
      stage('ArchiveArtifact') {
        steps{
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        }
      }
    
    
    
  }
  
}
