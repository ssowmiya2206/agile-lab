pipeline {
 agent any
 parameters {
 string(name: 'BRANCH_NAME',
 defaultValue: 'main',
 description: 'Git branch')
 string(name: 'NUM1',
 defaultValue: '10',
 description: 'First Number')
 string(name: 'NUM2',
 defaultValue: '20',
 description: 'Second Number')
 }
 stages {
 stage('Checkout') {
 steps {
 git branch: "${params.BRANCH_NAME}",
 url: 'https://github.com/Ramlingams/pipeline-parameters.git'
 }
 }
 stage('Addition Build') {
 steps {
 bat "python add.py ${params.NUM1} ${params.NUM2}"
 }
 }
 }
}
