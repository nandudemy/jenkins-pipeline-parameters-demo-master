pipeline {
    agent any
    parameters {
      booleanParam(
        name: 'CAN_DANCE',
        description: 'Deploy to QA',
        defaultValue: false
      )
    }    

    stages {
        stage('Checkout') {
          steps {
            echo "QA Build is ${params.CAN_DANCE}"
          }
        }
    }  

}
