node {
  def app

  stage('Clone repository') {
    checkout scm
  }

  stage('Build image'){
    app = docker.build("kadi08/pipeline1")
    }

  stage ('Push image'){
    docker.withRegistry('https://registry.hub.docker.com','docker-hub-credentials'){
      app.push("lastest")
    }
  }
}
