# Prisme's Tech-Radar

The [Tech Radar](http://www.techradar.prisme.as) describes the technology landscape through a Prisme lens. We've made this repo public partly because it helps us use the technology that generates the radar, and partly because it's interesting to see the technology we use at Prisme.

If you're going to build a new service, the Tech Radar gives you an idea of our default favoured stack. It is intended to apply to Prisme's actively developed products. We're not making any statements about retiring any technology (though teams are encouraged to regularly have these discussions!).

The [Tech Radar](http://techradar.prisme.com) describes the technology landscape through a Prisme lens.  We capture technology in one of four categories:
* Languages and Frameworks. Languages and frameworks that we use when building products.
* Tools. These can be components, such as databases, software development tools, such as versions control systems; or more generic categories of tools, such as the notion of polyglot persistence.
* Platforms. Things that we build software on top of such as .NET, SQL Server, Windows (etc).
* Techniques. These include elements of a software development process, such as experience design; and structuring software, such as microservices.

Items on the Tech Radar should only be captured if the cost of change is high or the benefits of standardizing outweigh the drawbacks. Each item on the tech radar should be there for the the good of Prisme or our customers.

Each technology choice is positioned in one of four areas.
* Adopt – We feel strongly that Prisme should be adopting these items. It’s the default choice.
* Trial – Worth pursuing. It’s important to understand how to build up this capability. Prisme teams can try this technology on a project that can support the risk.
* Assess – Worth exploring with the goal of understanding how it will affect Prisme
* Hold - Proceed with caution

The Tech Radar doesn’t provide all the answers, but it should give strong direction in those areas where choice makes a difference. For example, should we be favouring REST API´s over GraphQL? Are we adopting TypeScript? 

We're following Thoughtworks approach. For discussion on the quadrants, please see the [Thoughtworks Radar Faq](https://www.thoughtworks.com/radar/faq)

## What isn’t on the Tech Radar?
We only use the Tech Radar to capture decisions relevant to our growth products (those that we are investing in for the future). We don’t use the Tech Radar to capture historical decisions that are no longer relevant. For example, we’d prefer to say the technology we use going forward rather than listing all failed attempts in the past.

We don't include libraries on the radar. For example, it's of negligible benefit to have a standardized library for dealing with date/time or for retrieving from a URL. However, it is beneficial to standardize libraries for sharing information between services. For example, if we produce a CSV file and two libraries have different escaping conventions; that might be a problem (obviously you'd hope the spec would cover it!). Similarly, if the choice of a library makes adoption of a recommend item harder then we'll try and signpost that. We'll capture these libraries as recommendations on the internal wiki.

Examples of things that probably SHOULD NOT be on the tech radar
* 

Examples of things that probably SHOULD be on the tech radar
* .NET 6 (makes our products more aligned)
* Platform technologies (it’s what we should be aligning towards)
* More opinionated UI technology (React)
* Azure DevOps vs Github Actions equivalent (affects CI/CD and so on)

## Who builds the radar?

The radar is open for anyone within Prisme to contribute. Before contributing please read the [Contributing Guidelines](.github/CONTRIBUTING.md).

The recommended way to propose a change or spark a discussion is to open a PR. Comments from all interested parties are more than welcome.

## How is the radar built?

We use [Thoughtworks Tech Radar](https://radar.thoughtworks.com/) to generate our Tech Radar. The radar is backed by a single CSV file (that should nicely [render](https://help.github.com/articles/rendering-csv-and-tsv-data/)). CSV files are parsed using `d3.js` so please see their [documentation](https://d3-wiki.readthedocs.io/zh_CN/latest/CSV) for escaping rules. All changes to the Tech Radar should be completed via a PR and merged by someone else.

You can see the latest version at [techradar.prisme.as](http://techradar.prisme.as).

The audience for this is all technical development at Prisme. It's purpose is to help us to align our technical software/practices to build greater consistency at Prisme. 

The radar is less appropriate for early stage products where we are still finding product/market fit (the concerns are less likely to be technical at this stage) though we still recommend it as a good set of default options. Our intention is that products we commit to develop/sell adhere to the tech stack in this radar.

## Frequently Asked Questions

### How do I contribute?
Make a PR and it'll start a conversation in #tech-radar channel!

### It won't display properly. Help!

Common causes of this happening are:
* Leaving blank lines at the bottom (make sure these are removed)
* Forgetting to add a column (verify this by viewing it in GitHub's CSV display)
* Bad escaping
