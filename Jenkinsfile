node {
    stage('Debug') {
        sh 'pwd'
        sh 'ls -R'
    }
    stage('Build') {
        sh 'python3 -m py_compile ./sources/add2vals.py ./sources/calc.py'
    }
}