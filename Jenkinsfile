pipeline {
    agent any
    parameters {
      booleanParam(
        name: 'CAN_DANCE',
        description: 'Deploy to QA param ',
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
