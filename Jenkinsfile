@Library('jenkins-shared-library') _

// create variable of map type and set the values

def configMap = [
    type: "nodejsEKS", // type of the project based on this type pipeline will trigger from shared library
    component: "backend", // component of the project
    project: "expense"  // project name
]

pipelineDecission.decidePipeline(configMap)
// First this will trigger the pipelineDecissionMaker method from shared library