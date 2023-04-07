pipeline {

    agent any
     stage {

        stage (git Checkout) {
            steps {
                git branch: 'main', url: 'https://github.com/venkataprasanna45/demo-counter-app.git'
            }
        }
     }
}
