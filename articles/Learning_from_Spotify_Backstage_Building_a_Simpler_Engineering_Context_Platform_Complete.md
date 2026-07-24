# Learning from Spotify Backstage: Building a Simpler Engineering Context Platform

Modern engineering teams rely on many different tools: source-code
repositories, wikis, dashboards, deployment platforms, API
documentation, monitoring systems, cloud services, and internal portals.
The list grows quickly, and the information engineers need becomes
spread across multiple locations.

This article shares the motivation behind **Service Compass**, an
open-source project created by Codelitz. It is not intended to replace
existing developer portals. Instead, it explores a simpler approach to
helping engineering teams quickly find the information they need every
day.

## The Problem

In many companies, the web browser becomes the main navigation tool.
Engineers save bookmarks for repositories, infrastructure dashboards,
documentation, metrics, and other internal resources. Over time, each
person builds their own collection of links, but this knowledge remains
fragmented and difficult to share.

Even simple questions can take longer than expected:

-   Which team owns this service?
-   Where is the repository?
-   In which environments is the service running?
-   Where can I find its API documentation?
-   Which dashboard contains its logs and metrics?
-   Which deployment tool manages it?
-   What internal tools and services are available?

This becomes especially visible when a new developer joins the company
or moves to another team. Someone must explain the organization's tools,
identify the relevant services, share documentation, provide links, and
show where everything can be found.

The problem is not necessarily that the information does not exist. The
problem is that it is distributed across many systems without a clear
and consistent entry point.

## Discovering an Existing Solution

While reading Cloudflare's article, *The AI Engineering Stack We Built
Internally --- on the Platform We Ship*, I noticed a reference to
**Spotify Backstage**. Although the article focuses on Cloudflare's
internal AI engineering platform, it introduced me to a project that
addresses a challenge shared by many engineering organizations: bringing
together the information engineers need to understand and operate their
services.

Spotify Backstage is a mature and comprehensive open-source developer
portal. It centralizes service ownership, documentation, repositories,
infrastructure, and many other engineering resources in one place. Its
plugin architecture allows teams to integrate Grafana, Kubernetes, CI/CD
platforms, documentation systems, and many other internal tools.

I highly recommend exploring Backstage and understanding the problems it
solves.

However, adopting such a platform also requires investment.
Organizations need time to configure the platform, integrate their
ecosystem, and often develop custom plugins. For many companies, that
investment is absolutely worthwhile.

Reading about Backstage inspired a different question:

> **What if some engineering teams only need a lightweight engineering
> context platform instead of a fully extensible developer portal?**

That question became the starting point for **Service Compass**.

## The Solution

Service Compass is an open-source project created by Codelitz with a
simple goal: provide engineers with a single place to quickly find the
information they need about a service.

Instead of replacing existing tools, Service Compass acts as an
engineering context platform. It centralizes links to repositories,
documentation, environments, dashboards, metrics, API documentation,
deployment tools, and service ownership, making this information easy to
discover and navigate.

The initial version intentionally focuses on the most common engineering
needs. Rather than providing a large ecosystem of integrations and
plugins, it aims to offer a lightweight solution that is easy to deploy,
easy to maintain, and simple to understand.

By releasing the project as open source, the intention is to encourage
collaboration, share ideas with the engineering community, and provide a
practical starting point for teams facing similar challenges.

## Why Open Source?

Engineering teams across different companies often face the same
problems. While every organization has its own processes and tools, the
challenge of discovering engineering context is remarkably similar.

Making Service Compass open source allows the community to contribute
ideas, suggest improvements, and adapt the project to different
environments. It also creates an opportunity to learn from how other
teams solve the same problem.

The objective is not only to publish code, but also to share engineering
ideas and encourage discussion around developer experience.

## Future Direction

Service Compass is still in its early stages, but the long-term vision
extends beyond a catalog of services.

Future versions may include:

-   Repository metadata and ownership synchronization.
-   Architecture and dependency visualization.
-   AI-assisted summaries of services and repositories.
-   Modernization insights for engineering teams.
-   Optional integrations with popular engineering platforms while
    keeping the project lightweight.

The goal is to help engineers understand systems faster without
replacing engineering judgment. Existing tools already perform their
individual tasks very well. Service Compass aims to become the place
that connects them together and provides the engineering context that is
often missing.

## Final Thoughts

Service Compass is not intended to compete with platforms such as
Spotify Backstage. It was inspired by them and explores a different
point in the design space: a lightweight, focused, and easy-to-adopt
engineering context platform.

If your team already benefits from Backstage, that's an excellent
choice. If you're looking for a simpler starting point, Service Compass
may be worth exploring.

Every engineering team solves similar problems in different ways.
Service Compass is my attempt to simplify one of them. If your team
approaches engineering context differently, I'd genuinely be interested
in hearing about it.

------------------------------------------------------------------------

## References

-   Cloudflare --- *The AI Engineering Stack We Built Internally --- on
    the Platform We Ship*
    https://blog.cloudflare.com/internal-ai-engineering-stack/

-   Spotify Backstage https://backstage.io/

-   Service Compass Repository
    https://github.com/codelitzlabs/service-compass
