node {

    parameters {
      booleanParam(
        name: 'isQABuild',
        description: 'Deploy to QA',
        defaultValue: false
      )
    }    

  stage('Checkout') {
    checkout scm
   
  }
    
    if (env.isQABuild){
         stage("QA Build"){
            echo "Running QA Build"
         }
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
