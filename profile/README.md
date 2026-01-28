![DriftlessAF logo](./driftlessaf-small.png)

# DriftlessAF

DriftlessAF is an agentic framework that enables bots to use traditional and
agentic AI eval approaches for reconciliation automation at massive scale.

DriftlessAF consists of Terraform modules for the event-driven reconciliation
infrastructure and Go packages for the agentic foundation. 

The Terraform modules include the generic core reconciler, a multi-regional work
queue, and a reconciler for resources at specific paths in GitHub repositories.

The Go packages include executors for Google Gemini and Anthropic Claude,
evaluators for tracing and metrics, and Go libraries to facilitate
reconciliation across GitHub repositories, OCI containers, and APK packages.

Using DriftlessAF you can configure the desired state, configure reconciler
bots, and affected system, such as source code in GitHub repositories. The
framework can then monitor state and the traditional and agentic AI reconciler
bots can queue work items and the automated processing will avoid any drift off
the desired state.

## Practical use

Chainguard uses DriftlessAF as the foundation for numerous custom reconciler
bots in Chainguard Factory. The factory is used to build and maintain over 2000
unique containers, hundreds of thousands of package versions, and hundreds of
CVE patch backports. DriftlessAF replaces a legacy event-driven architecture and
is critical to achieve the necessary efficiency and reliability at scale. 

The work queue is fed by events and tackled by a large number of bots. They
constantly reconcile the discovered state changes from code repositories,
security feeds, and other sources to the desired state - up to date containers
with zero known CVEs. 

## Projects

* [terraform-infra-reconcilers](https://github.com/driftlessaf/terraform-infra-reconcilers)
  provides Terraform modules for the reconciler infrastructure
* [go-driftlessaf](https://github.com/driftlessaf/go-driftlessaf) provides Go
  implementations for LLM execution and evaluation in the framework and
  libraries to facilitate reconciliation across GitHub repositories, OCI
  containers, and APK packages.

## Open source and community

The DriftlessAF open source project provides a production-grade framework for your
own use. Note that the project is primarily offered for read-only access,
inspection, and expansion with your own bots for your specific use cases.

We currently do not have plans for community calls or active community
development. Contact us if you use DriftlessAF or are interested in further
collaboration and contribution.

## Contact

* Find us to chat live on the `questions` channel in the [Chainguard Community
  on Slack](https://communityinviter.com/apps/chainguardcommunity/invite)
* Ask questions and discuss related topics such as bug fixes or feature
  proposals on [GitHub
  discussions](https://github.com/orgs/driftlessaf/discussions)
