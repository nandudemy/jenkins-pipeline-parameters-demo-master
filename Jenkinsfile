pipeline {

    parameters {
      booleanParam(
        name: 'CAN_DANCE',
        description: 'Deploy to QA',
        defaultValue: true
      )
    }    

  stage('Checkout') {
    echo "QA Build is ${params.CAN_DANCE}"
  }
  

}
