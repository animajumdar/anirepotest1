pipeline {
  agent none
  stages {
    stage('testbuild') {
      steps {
        echo 'test build'
      }
    }

    stage('test done') {
      steps {
        echo 'test done'
      }
    }

    stage('test python version') {
      agent { label 'execnode1' }
      steps {
          bat """
            cd C:\\testrepo1\\atlas-probe\\test_suites\\BASELINE
            set PYTHONPATH=C:\testrepo1\atlas-probe\atheneum
            set https_proxy=http://web-proxy.in.hpecorp.net:8080
            set http_proxy=http://web-proxy.in.hpecorp.net:8080
            python -m pytest -c ../../test_config/config.ini  ../../test_config/ --pyargs ../../test_cases --tags="input_tag.txt" --html=report.html
          """
      }
    }
  }
}
