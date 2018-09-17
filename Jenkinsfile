pipeline {
  agent any
  parameters {
    choice(name: 'Namespace_Choice',
      choices: 'Merch-pl-planning-ci\nMerch-pl-planning-stage-3\nMerch-pl-planning-stress-3\nMerch-pl-planning-preprod',
      description: 'Select the required Namespace')
    booleanParam(name: 'NAMESPACE_LIST',
      defaultValue: false,
      description: 'Checkbox parameter'),
	  booleanParam(name: 'NAMESPACE_LIST',
      defaultValue: false,
      description: 'Checkbox parameter')
    string(name: 'sTrAnGePaRaM',
      defaultValue: 'Dance!',
      description: 'Do the funky chicken!')
  }
  stages {
    stage('Example') {
      steps {
        echo 'Hello World!'
        echo "Trying: ${params.Namespace_Choice}"
        echo "We can dance: ${params.NAMESPACE_LIST}"
        echo "The DJ says: ${params.sTrAnGePaRaM}"
      }
    }
  }
}
