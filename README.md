# CDK

Cloud Development Kit.

为了避免通过各种DSL来管理资源，而且DSL有各种限制。

CDK为开发者通过自己喜欢的编程语言来管理资源提供了可能，而且能深度定制。

比如AWS通过cloudformation来管理资源，需要编写cf文件。

比如k8s需要通过yaml来管理k8s资源。

比如terraform需要通过tf文件来管理资源。

## AWS CDK

用来创建和管理云上的基础设施： VPC, EKS, ManagedNodeGroup, Fargate Profile...

aws cdk 能将开发者的代码编译为cloudformation支持的格式来管理资源。

## CDK8S

用来管理K8S上的资源： namespace, pod, deploy, service, daemonset, jobs, ingress...

cdk8s能将开发者的代码编译为k8s支持的yaml文件来管理k8s资源。

## CDKTF

用来管理terraform资源（管理云基础设施，或者管理k8s资源）。

cdktf能将开发者的代码编译为terraform支持的tf格式文件来管理资源。

    // create project.
    cdktf init --template="go"
    // get terraform provider.
    cdktf get
    // install go pkg.
    go mod tidy
    // provision resource.
    cdktf deploy
    // generate files can be used by terraform.
    cdktf synth
    // remove resource.
    cdktf destroy
