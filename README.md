# CRD - what is it?
A CRD is a custom resource definition.

# How is it used?
It's used to declare custom resources, which can be used by
controllers (control-loops that watch the state of the cluster).

# Operators
Typically written in golang (see operatorSDK), these provide
CRD's and controllers.
e.g. flux provides the HelmChart CRD, which
is managed by flux controllers to configure the state of the cluster.

CRD + controller = operator

The flux controller (source of action) will perform changes on the cluster
based on the CRD's that are declared (source of information).
