pipeline {
  agent none
  stages {
    stage('pre') {
      steps {
        echo 'This is jenkins file test'
        git(url: 'http://gitlab.prod.dtstack.cn/mufeng/interfaceTestBase.git', credentialsId: '8ce394ce-66e7-4f00-9bb1-4f4f6d4a5b81', changelog: true, branch: '*/master')
      }
    }

    stage('build') {
      steps {
        sh 'sh \'"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package\''
      }
    }

  }
}
