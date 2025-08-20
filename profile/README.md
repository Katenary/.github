>  ⚠️ **PROJECT HAS MOVED**
> 
>  ⚠️ **Katenary has moved to https://repo.katenary.io/Katenary, please update your bookmarks.**
>
> See the discussion here https://github.com/orgs/Katenary/discussions/162

## Katenary 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
Katenary is a tool to convert your compose files to Helm Chart. Work with Podman, Docker, NerdCtl as usual. Then, Katenary produces a customizable Helm Chart ready to be depolyed on your Kubernetes cluster.

Simple, useful, efficient.

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
