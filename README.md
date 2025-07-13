# Katenary

Effortless Helm Chart Conversion for Kubernetes Deployments

## Why Katenary?
Simplify your deployment workflow by converting Compose files into production-ready Helm Charts with ease.

- Automated Conversion
Generate complete Helm Charts from your Compose files effortlessly.
- Flexible Configuration
Customize deployments with `values.yaml` and environment labels.
- Dependency Management
Ensure proper service startup sequences using `depends_on` support.
- Open Source
Free, opensource, under the MIT license!


How It Works
Katenary simply read your compose.yaml file (or docker-compose.yaml) and use official libraries to read it and generate Kubernetes resources as YAML.

Then, it adds templating conditions, values file, define a Chart.yaml file, adapt dependencies if needed, and many others things.

Using configuration files to be mounted? No problem, Katenary will create ConfigMaps if you declared that thes directories or files are statics.
(Do not do this for sources of your project, use it for simple configuration files)

The result is a complete "Helm Chart" that can be installed, configured, packaged and shared.

![](https://github.com/Katenary/katenary/raw/refs/heads/develop/doc/docs/statics/workflow.svg)

Katenary Workflow
Almost everything can be overriden as Ingresses, Dependencies, values, environment variables, secrets...

1. Add optional labels to your Compose files.
1. Run katenary convert from the command line.
1. Deploy the generated Helm Chart in Kubernetes.
