pipeline {
  agent any

  environment {
    // 定义环境变量
    COMPONENTS = ['None','nginx']
  }

  parameters {
    choice(name: 'Component', choices: ${env.COMPONENTS}, description: '要构建的环境组件')
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
