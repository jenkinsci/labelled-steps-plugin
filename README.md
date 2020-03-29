# labelled-steps-plugin

Currently this plugin provides a replacement for the [`sh`] [sh], [`bat`][bat] and [`powershell`][powershell] steps in Jenkins
pipelines to allow displaying a custom label in the BlueOcean UI.


### Why is this needed?

See [JENKINS-36933][] and [JENKINS-37324][].


### Example

In the following example, the BlueOcean UI will display `Building the universe from scratch...`
as the step title (the step title is the thing you click on to see the shell output):

```groovy
labelledShell label: 'Building the universe from scratch...', script: """
    echo "Sparking the Big Bang..."
    echo "Cosmic inflation begins..."
    # ...
"""
labelledBatch label: 'Building the universe from scratch...', script: """
    echo "Sparking the Big Bang..."
    echo "Cosmic inflation begins..."
    # ...
"""
labelledPowerShell label: 'Building the universe from scratch...', script: """
    echo "Sparking the Big Bang..."
    echo "Cosmic inflation begins..."
    # ...
"""
```




[sh]: https://jenkins.io/doc/pipeline/steps/workflow-durable-task-step/#sh-shell-script
[bat]: https://jenkins.io/doc/pipeline/steps/workflow-durable-task-step/#bat-windows-batch-script
[powershell]: https://jenkins.io/doc/pipeline/steps/workflow-durable-task-step/#powershell-powershell-script
[JENKINS-36933]: https://issues.jenkins-ci.org/browse/JENKINS-36933
[JENKINS-37324]: https://issues.jenkins-ci.org/browse/JENKINS-37324
