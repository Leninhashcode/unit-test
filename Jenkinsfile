pipeline {
    agent any

    stages {
      stage ("clone"){
        steps {
            "git 'https://github.com/Leninhashcode/unit-test'"

        }
      }
      stage("check"){
        steps {
            sh "ls -ltr"
        }
      }
      stage("requirements"){
        steps{
                sh '''
                python3 -m pip install --upgrade pip
                pip3 install -r requirements.txt
                pip3 install pytest
                '''

            
        }
      }
      stage ("test"){
        steps{
            sh "pytest"
        }
      }
      stage("last"){
        steps{
            echo "done"
        }
      }
        
        
    }
}