pipeline {
  agent any

  parameters {
    choice(name: 'Component', choices: ['nginx'], description: '要构建的环境组件')
  }

  stages {
    stage('Echo Component') {
      steps {
        echo "构建组件: ${params.Component}"
      }
    }
  }

  post {
        always {
      echo 'Pipeline执行完成'
        }
        success {
      echo 'Pipeline成功!'
        }
        failure {
      echo 'Pipeline失败!'
        }
  }
}
