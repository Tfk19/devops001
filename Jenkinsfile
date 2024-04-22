pipeline {
  agent {
    node {
      label 'Fahri'
    }

  }
  stages {
    stage('Berdiskusi') {
      parallel {
        stage('Berdiskusi') {
          steps {
            build 'cari salah'
          }
        }

        stage('') {
          steps {
            waitUntil(initialRecurrencePeriod: 1, quiet: true) {
              sleep 20
            }

          }
        }

      }
    }

    stage('Menemukan Kesalahan') {
      steps {
        node(label: 'Menemukan Kekurangan')
      }
    }

    stage('Selesai') {
      steps {
        cleanWs(cleanWhenAborted: true)
      }
    }

  }
}