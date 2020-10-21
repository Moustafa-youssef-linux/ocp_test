// TODO: run this simple pipeline on jenkins 'master' node
agent {
  node {
    label 'master'
  }
}

stage('Build') {
  steps {
    sh 'echo hello from Build stage '
  }
}



stage('Test') {
  steps {
    sh 'echo hello Test stage 2!'
  }
}

stage('Deploy') {
  steps {
    timeout(time: 60, unit: 'MINUTES') {
      input message: "Move to stage 3?"
    }
  }
}
