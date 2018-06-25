# Improving the Customization Process for Variability Intense Software

## Solution Approach

### Platform Variability Model

The following image shows a detail of the FeatureModel for the Tool Integration Platform of the industry partner. For example, the model defines the abstract optional feature _Commit_. The feature names, which must be unique in the model, are derived from the component names for simplicity. The branch of the _Commit_ feature is optional as it can be omitted in the final version if, for example, the quality assurance activities are not needed at all in an engineering process. The two abstract features _AML-Commit_ and _File-Commit_ descend from the quality interface bundle and are thus children and concrete features of the _Commit_ feature.
Constraints in the feature model, represent dependencies amongst interfaces and services. In the figure the constraints can be found above the legend of the model or within the model using the the graphical notation. For instance, if a process is selected that manipulates a model, a service that can check in models into the database is required.

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
