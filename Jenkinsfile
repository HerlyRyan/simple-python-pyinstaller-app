node {
    stage('Checkout') {
        checkout scm
    }
    stage('Debug') {
        sh 'pwd'
        sh 'ls -R'
    }
    stage('Build') {
        sh 'python3 -m py_compile ./sources/add2vals.py ./sources/calc.py'
    }
    stage('Test') {
        try {
            sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
        } finally {
            junit 'test-reports/results.xml'
        }
    }
}