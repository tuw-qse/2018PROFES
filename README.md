# Improving the Customization Process for Variability Intense Software

## Solution Approach

### Platform Variability Model

![Platform Feature Model Detail](images/fm-checkin-profes.pdf "Platform Feature Model")

### Process Variability Model

The following image shows the UML Representation of the ``ServiceTask`` and its relation to the ``Operation``.

![UML Meta-Model - BPMN ServiceTask](images/serviceTask.pdf "BPMN ServiceTask")

Instead of referring a concrete service instance name, that is resolved by the workflow engine, the ``bpmn:serviceTask`` is enriched with the name of a feature from the feature model and prefixed with the ``abstract`` keyword, as shown in the code snippet below.

```
<bpmn:serviceTask id="2" name="Compare AML" operationRef="abstract:AMLComparison">
```
With this adaptation, we can build business process blueprints that can than be used during the customization process as templates.

## Discussion

![Relation Improvement](images/diagram.pdf "Relation Improvement")
