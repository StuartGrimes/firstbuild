pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Starting to create a file...ensuring no directories present'
                sh 'rm -rf ./*'
                sh 'mkdir build'
                sh 'touch build/car.txt'
                sh 'echo "engine" >> build/car.txt'
                sh 'echo "chassis" >> build/car.txt'
                sh 'echo "body" >> build/car.txt'
            }
        }
        stage('testing'){
            steps{
                sh 'grep "engine" ./build/car.txt'
                sh 'grep "chassis" ./build/car.txt'
                sh 'grep "body" ./build/car.txt'
            }
        }
    }
}