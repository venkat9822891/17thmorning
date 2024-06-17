node {
    stage('Download') {
         git branch: 'dev', url: 'https://github.com/venkat9822891/17thmorning.git'
                       }
     stage('ConvertArtifacts') {
         sh 'mvn package' 
         }
     stage('Deployment in DevEnv') {
           deploy adapters: [tomcat9(credentialsId: '5b3f6c06-b39a-4e72-86b1-d250ba8125b4', path: '', url: 'http://172.31.7.78:8080')], contextPath: '/devapps', war: '**/*.war'
         }
     }
