# IBM-FileNet-WorkflowTestFramework
A TestNG Framework to be able to Unit Test IBM FileNet workflows

# Usage
To test if the workflow object is at a specific step, use the __assertAtStep__. Verify the settability of a parameter with __asserParameterIsReadWriteable__ or __assertParameterIsNotReadable__

For instance
```
public void testVerifyAtStepEnterValues() {
    String atStepName = "Enter case value";
    VWWorkObject wob = ops.getWorkObject();

    assertAtStep(wob, atStepName);
    assertParameterIsReadWriteable(wob, "CaseValue");
    assertParameterIsReadWriteable(wob, "CaseName");
    assertParameterIsNotReadable(wob, "IsApproved");
}
```

# Additional resources

http://www.patrickvanderhorst.info/blogs/filenet-workflow-test-framework-(part-1-of-3).html
http://www.patrickvanderhorst.info/blogs/filenet-workflow-test-framework-(part-2-of-3).html
http://www.patrickvanderhorst.info/blogs/filenet-workflow-test-framework-(part-3-of-3).html
