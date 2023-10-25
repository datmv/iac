pipeline{
    stage any
        parameters {
            string defaultValue: 'DC', name: 'DC'
            choice choices: ['node-1'], name: 'node-1'
    }
    stages{
        stage{
            echo "hi ${node-1}"
        }
    }
}