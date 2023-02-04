// pipeline {
//     agent any
//        stages {
//           stage('Clone Repository') {
//            steps {
//               git branch: 'PROD',
//               credentialsId: 'sidrakiran',
//               url: 'https://github.com/sidrakiran2/PROJECT.git'
//             }
//            }
//          stage('Build Docker Image') {
//            steps {
//            sh 'docker build -t sidra22/docker_pipeline .'
//            }
//             }
//         stage('Push to Docker Hub') {
//      steps {
//    sh 'docker login -u sidra22 -p sidra@123'
//       sh 'docker push sidra22/docker_pipeline'
//     }
pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'PROD',
                credentialsId: 'sidrakiran',
                url: 'https://github.com/sidrakiran2/PROJECT.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sidra22/docker_pipeline .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                sh 'docker login -u sidra22 -p sidra@123'
                sh 'docker push sidra22/docker_pipeline'
            }
        }
        
    }
}