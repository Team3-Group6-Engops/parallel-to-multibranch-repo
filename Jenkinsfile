pipeline{
    agent any 
    stages{
        stage('clone-stage'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/Team3-Group6-Engops/parallel-to-multibranch-repo.git']]])
            }
        }
        stage('parallel-1'){
            parallel{
                stage('abayomi-parallel-stage'){
                    steps{
                     sh 'whoami'
                     echo "I am a Devops Engineer"
                    }
                }
                stage('abayomi-parallel2'){
                    steps{
                        echo "This is a parallel pipeline"
                    }
                }
            }
        }
        stage('parallel-2'){
            parallel{
                stage('check for OPS'){
                    steps{
                        sh 'lscpu'
                    }
                }
                stage('check-pwd'){
                    steps{
                        sh 'pwd'
                    }
                }
            }
        }  
        stage('parallel-3'){
            parallel{
                stage('claudi-parallel-stage1'){
                    steps{
                        sh 'cat /etc/passwd'
                        echo "My name is Claudi"
                    }
                }
                stage('claudi-parallel-stage2'){
                    steps{
                        sh 'chmod +x claudi.sh'
                        sh 'bash -x claudi.sh'
                    }
                }
            }
        }
        stage('parallel-4'){
            parallel{
                stage('Annick-parallel-stage1'){
                    steps{
                        echo "I am an Etech Devops Master"
                    }
                }
                stage('user-check-stage2'){
                    steps{
                        sh 'cat /etc/passwd | grep jenkins'
                    }
                }
            }
        }
    } 
}
