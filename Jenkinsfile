node {

  properties([
    parameters {
      choice(name: 'door_choice',
        choices: 'one\ntwo\nthree\nfour',
        description: 'What door do you choose?')
      booleanParam(name: 'isQABuild',
        defaultValue: false,
        description: 'Deploy to QA')
      string(name: 'sTrAnGePaRaM',
        defaultValue: 'Dance!',
        description: 'Do the funky chicken!')
    }    
  ])

  stage('Checkout') {
     checkout scm
  }

  if(env.BRANCH_NAME ==~ /feature.*/){
    stage("Deploy"){
       echo 'Performing Feature build'
    }
  }

  if(env.BRANCH_NAME == 'develop'){
    if (params.isQABuild){
      stage("Deploy"){
        echo 'Performing QA build'
      }
    } else {
      stage("Deploy"){
        echo 'Performing CI build'
      }
    }
  }

  if(env.BRANCH_NAME ==~ /release.*/){
    stage("Deploy"){
       echo 'Performing release build'
    }
  }


  if(env.BRANCH_NAME == 'master'){
    stage("Deploy"){
       echo 'Performing master build'
    }
  }
  
}
