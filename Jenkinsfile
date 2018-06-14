pipeline {
    agent any 
    stages {
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
        stage('Success Stage') {
            steps {
                echo 'IT WORX!'
            }
        }
    }
}

