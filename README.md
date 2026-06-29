# Franka Developer Portal

Welcome to the Franka Developer Portal — your central source for documentation
across all Franka software projects.

This book is **auto-generated** from each project's `docs/` directory.
Content is kept in sync by the [doc-converter](https://gitlab.franka.de/franka-dev/devportal/doc-converter)
pipeline, which runs whenever documentation changes are merged to `main`.

## Projects

| Project | Description |
|---------|-------------|
| [Alpha](content/alpha/index.md) | Robot Fleet Manager — control plane for Franka robot fleets |
| [Beta](content/beta/README.md) | Simulation Suite — Gazebo-based robot simulation |
| [Gamma](content/gamma/overview.md) | Gripper Intelligence — AI-powered grasp planning |

## How It Works

![DevPortal Architecture](../assets/devportal-architecture.svg)

1. Developer commits documentation changes to a project's `main` branch
2. GitLab CI detects changes in `docs/` and triggers the doc-converter pipeline
3. The converter container processes markdown, images, and assets
4. Converted content is pushed to this repository
5. GitBook (or a static site generator) picks up the changes

## Contributing

To add a new project to this portal:

1. Add a `docs/` directory to your project with markdown files
2. Add a `.gitlab-ci.yml` trigger (see `ci-templates/docs-pipeline.yml` in doc-converter)
3. The converter will pick it up on the next `main` branch commit

---
*Last updated: auto-generated — timestamp per page*
