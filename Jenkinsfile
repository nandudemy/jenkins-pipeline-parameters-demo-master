node {

  properties([
    parameters {
      booleanParam(
        name: 'isQABuild',
        defaultValue: false,
        description: 'Deploy to QA'
      )
    }    
  ])

  stage('Checkout') {
    checkout scm
    echo "Value of QA is: params.isQABuild" 
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
