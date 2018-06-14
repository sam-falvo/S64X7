pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
        stage('Compile') {
          steps {
            sh 'iverilog -I rtl/verilog bench/verilog/S64X7.v rtl/verilog/*.v'
          }
        }
        stage('RunTest') {
          steps {
            sh 'vvp -n a.out'
          }
        }
    }
}

