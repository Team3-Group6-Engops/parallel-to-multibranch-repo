pipeline{
    agent any 
    stages{
        stage('clone-stage'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/Team3-Group6-Engops/parallel-to-multibranch-repo.git']]])
            }
        }
        stage('conditional stage 1'){
           when{
               branch 'feature'
           }
           steps{
                echo "only run on feature branch"
           }
        }
        stage('parallel-1'){
            parallel{
                stage('abayomi-parallel-stage'){
                    steps{
                     sh 'whoami'
                     echo "I am a Devops Engineer!"
                    }
                }
                stage('abayomi-parallel2'){
                    steps{
                        echo "This is a parallel pipeline."
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
        stage('conditional stage 2'){
           when{
               branch 'develop'
           }
           steps{
                echo "only run on feature branch"
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
                        echo "I am a DevOps Engineer!"
                    }
                }
            }
        }
        stage('parallel-4'){
            parallel{
                stage('Annick-parallel-stage1'){
                    steps{
                        echo "I am an Etech Devops Master."
                    }
                }
                stage('user-check-stage2'){
                    steps{
                        sh 'cat /etc/passwd | grep jenkins'
                    }
                }
            }
        }
        stage('parallel-5'){
            parallel{
                stage('Frank-parallel-stage1'){
                    steps{
                        echo "My name is Frank Madu"
                    }
                }
                stage('Frank-parallel-stage2'){
                    steps{
                        echo "continue to practive DevOps" 
                    }
                }
            }
        }
        stage('conditional stage 3'){
           when{
               branch 'main'
           }
           steps{
                echo "only run on feature branch"
           }
        }
        stage('parallel-6'){
            parallel{
                stage('francisca-parallel-stage1'){
                    steps{
                        echo "welcome Eng. francisca "
                    }
                }
                stage('francisca-parallel-stage2'){
                    steps{
                        sh 'cat /etc/passwd'
                    }
                }
            }
        }
        stage('parallel-7'){
            parallel{
                stage('abbey-parallel-stage1'){
                    steps{
                        echo "welcome to Etech consulting"
                    }
                }
                stage('abbey-parallel-stage2'){
                    steps{
                        echo "I am a DevOps Engr."
                    }
                }
            }
        }      
    } 
}
