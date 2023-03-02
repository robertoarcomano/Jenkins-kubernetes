podTemplate(cloud: 'not-jenkins-source', label: 'hello-world' yaml: agentPodYaml.getWithContainers('python')) {
  node('hello-world') {
    sh "echo 'Hello World, I am running inside the Jenkins agent container'"
    container('python'){
      sh 'echo \'print("Hello from the python side.")\' > hello-world.py'
      sh 'python hello-world.py'
    }  
  }
}