pipeline {
    agent any


    parameters {

        string (name: 'LIB_BRANCH',
                defaultValue: 'master',
                description: 'Shared library branch')
            choice(
                name: 'Namespace',
                choices:"Merch-pl-planning-ci\nMerch-pl-planning-stage-3\nMerch-pl-planning-stress-3\nMerch-pl-planning-uat-3\nMerch-pl-planning-preprod",
                description: "Choose Namespace!")
            choice(
                name: 'GIT_BRANCH',
                choices:"release_1.0\nrelease_1.0_develop\nmaster",
                description: "Build for which version?" )
            choice(
                name: 'BUILD_APP',
                choices:"kap-admin-service\nkap-assortment-service",
                description: "Apps to be built!")
        	booleanParam(name: 'kap-admin-service',
        	 defaultValue: false,
        	 description: 'Choose sevice to build')
	         booleanParam(name: 'kap-assortment-service',
        	 defaultValue: false,
             description: 'Choose service to build')
            choice(
           name: 'Versions',
                   choices:"version_of_app1\nversion_of_app2",
                   description: "Versions to be deploy")
    }

    stages {
        stage("Parameter Build") {
            steps {
               script {
                     parameters {
                    [string(name: 'GIT_BRANCH', value: "${params.GIT_BRANCH}"),
                        string(name: 'Namespace', value: "${params.Namespace}"),
                         string(name: 'Versions', value: "${params.Versions}"),
                         string(name: 'LIB_BRANCH', value: "${params.LIB_BRANCH}"),
                         string(name: 'BUILD_APPS', value: "${params.BUILD_APPS}"),
                         string(name: 'BUILD_APPS', value: "${params.kapadminservice}"),
                         string(name: 'BUILD_APPS', value: "${params.kapassortmentservice}")]
                   }
            }
        }

    }
    }
}
    

