pipeline {
	 agent {
	     node {
 		label 'nodejs'
 	     }
 	}
 	stages {
 stage('Run Tests') {
 parallel {
 stage('Backend Tests') {
 steps {
 sh 'node ./backend/test.js'
 }
 }
 stage('Frontend Tests') {
	when { expression { params.RUN_FRONTEND_TESTS } } 
	steps {
 		sh 'node ./frontend/test.js'
 		}
 	}
 	}
 }
 }
}

