#!/usr/bin/env groovy
// @Library('apm@current') _

pipeline {
  agent { label 'linux || immutable' }
  environment {
    BASE_DIR = "."
    CI = true
    HOME = "${JENKINS_HOME}"
    // PR_SOURCE_BRANCH = "${ghprbSourceBranch}"
    // PR_TARGET_BRANCH = "${ghprbTargetBranch}"
    // PR_AUTHOR = "${ghprbPullAuthorLogin}"
  }
  stages {
    stage('Kickoff') {
      steps {
        sh 'env > env.txt' 
        script {
          for (String x: readFile('env.txt').split("\r?\n")) {
            println "# ENV VAR: ${x}"
          }
        } 
        dir("${env.BASE_DIR}"){
            sh './.ci/run.sh'
        }
        stash allowEmpty: true, name: 'source', useDefaultExcludes: true
      }
    }
    stage('Static Analysis') {
      steps {
        sh 'echo "Not implemented yet"'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'echo "Not implemented yet"'
      }
    }
    stage('Component Integration Tests') {
      steps {
        sh 'echo "Not implemented yet"'
      }
    }
    stage('Functional Tests') {
      steps {
        sh 'echo "Not implemented yet"'
      }
    }
    stage('Finish') {
      steps {
        sh 'echo "Not implemented yet"'
      }
    }
  }
}