node{
    stage('pull from git') {
        sh "echo pull from git"
    }
    stage('build') {
        sh "echo Build"
    }
    stage('test'){
      parallel (
        "Unit": {
            sh "echo unit"
        },
        "Functional": {
            sh "echo Functional"
        }
      )
    }
    stage('dev'){
         sh "echo deploy dev functional"
    }
    stage('Sanity check') {
         input "Does the staging environment look ok?"
    }
    stage('staging'){
         sh "echo stage functional"
    }
}