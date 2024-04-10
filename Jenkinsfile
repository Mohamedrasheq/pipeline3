pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Checkout the code from your Git repository
                bat 'https://github.com/Mohamedrasheq/pipeline3.git'
                
                // Build the Maven project
                bat 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                // Run Maven tests
                bat 'mvn test'
            }
        }
        stage('Run') { 
            steps {
                bat 'java -cp target/classes com.example.bubblesort.BubbleSort'
            }
        }
    }
}
