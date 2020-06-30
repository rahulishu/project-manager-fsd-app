node {
 

        stage('Checkout') {
            git url: 'https://github.com/rahulishu/project-manager-fsd-app.git',  branch: 'master'
        }

        stage('node modules') {
            sh 'npm install'
        }

        stage('Test') {
            sh 'ng test --progress=false --watch false'
        }

        stage('Build') {
            sh 'ng build --prod --aot --sm --progress=false'
        }

        stage('Image') {
            dir ('project-manager-fsd-app') {
                def app = docker.build "project-manager-fsd-app:${env.version}"
                app.push()
            }
        }

        stage ('Run') {
            docker.image("project-manager-fsd-app:${env.version}").run('-p 4200:4200 -h project-manager-fsd-app --name project-manager-fsd-app')
        }    

}
