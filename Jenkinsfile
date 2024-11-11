pipeline {
    agent any 

    parameters {
        // Định nghĩa các tham số đầu vào cho pipeline
        string(name: 'REPO_URL', defaultValue: 'https://github.com/nguyen-van-tien0601/1.git', description: 'URL của repository Git')
        string(name: 'BRANCH', defaultValue: 'main', description: 'Tên branch bạn muốn checkout')
        //string(name: 'CREDENTIALS_ID', defaultValue: 'git-credentials-id', description: 'ID của credentials Git (nếu cần authentication)')
    }

    stages {
        stage('Checkout SCM') {
            steps {
                script {
                    // Sử dụng tham số từ pipeline để checkout mã nguồn
                    echo "Checkout repository from ${params.REPO_URL} on branch ${params.BRANCH}"

                    // Kiểm tra nếu cần sử dụng credentials
                    // if (params.CREDENTIALS_ID) {
                    //     // Sử dụng các credentials để thực hiện checkout (nếu cần)
                    //     myRepo = checkout([
                    //         $class: 'GitSCM',
                    //         branches: [[name: "refs/heads/${params.BRANCH}"]],
                    //         userRemoteConfigs: [[url: params.REPO_URL, credentialsId: params.CREDENTIALS_ID]]
                    //     ])
                    // } else {
                        // Nếu không cần credentials, thực hiện checkout mà không cần authentication
                        myRepo = checkout([
                            $class: 'GitSCM',
                            branches: [[name: "refs/heads/${params.BRANCH}"]],
                            userRemoteConfigs: [[url: params.REPO_URL]]
                        ])
                    //}
                }
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                // Các bước build sẽ ở đây
            }
        }

        // Các stage khác...
    }
}
