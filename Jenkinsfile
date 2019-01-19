node {

    parameters {
      booleanParam(
        name: 'CAN_DANCE',
        description: 'Deploy to QA',
        defaultValue: true
      )
    }    

  stage('Checkout') {
    checkout scm
    echo "QA Build is ${params.CAN_DANCE}"
  }
  

  if(env.BRANCH_NAME ==~ /feature.*/){
    stage("Deploy"){
       echo 'Performing Feature build'
    }
  }

  if(env.BRANCH_NAME == 'develop'){
      stage("Deploy"){
        echo 'Performing CI build'
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
