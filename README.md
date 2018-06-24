# Improving the Customization Process for Variability Intense Software

## Solution Approach

### Process Variability Model

The following image shows the UML Representation of the ``ServiceTask`` and its relation to the ``Operation``.

![UML Meta-Model - BPMN ServiceTask](images/serviceTask.pdf "BPMN ServiceTask")

Instead of referring a concrete service instance name, that is resolved by the workflow engine, the ``bpmn:serviceTask`` is enriched with the name of a feature from the feature model and prefixed with the ``abstract`` keyword.

```
<bpmn:serviceTask id="2" name="Compare AML" operationRef="abstract:AMLComparison">
```

## Discussion

![Relation Improvement](images/diagram.pdf "Relation Improvement")
