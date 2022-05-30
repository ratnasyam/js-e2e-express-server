pipeline{
    
    agent{
        label'node_js_11'
    }
    stages{
        stage('scm'){
            git branch: 'main' , url: 'https://github.com/ratnasyam/js-e2e-express-server.git'
        }
        stage('build'){
            sh ''' npm install
                   npm run build
                   npm pack'''
        }
    }
    post{
        success{
            archive '**/*.tgz'
        }
    }

}
 