# Publishing notes

## Recommended home

The public framework lives in the standalone GitHub repository:

```text
https://github.com/aikoucka-bot/relational-agent-collaboration-framework
```

Keeping the repository separate from the personal vault prevents internal history, private context, and client material from entering the public artifact.

## Why GitHub

- Markdown works without another publishing system.
- Version history preserves the framework's development.
- Issues or Discussions can collect examples, objections, and proposals.
- Releases can mark stable versions.
- `CITATION.cff` provides machine-readable citation metadata.
- GitHub Pages can later provide a more readable site from the same source.

GitHub recommends a README that explains purpose, value, first steps, support, and maintainers. A license, citation file, and contribution guidance clarify expectations.

## Possible publication stages

### 1. Public draft

- publish the reviewed English and Czech texts,
- keep the status visible as `0.1.0-draft`,
- collect substantive corrections before treating the framework as stable.

### 2. Stable v0.1

- complete the authors' semantic review,
- remove unintended placeholders and internal notes,
- verify links and Markdown,
- add a concise `CHANGELOG.md` if version history needs a human-readable summary,
- create a GitHub release.

### 3. Citable version

Zenodo can connect to GitHub and archive releases with a DOI. This becomes useful when the authors consider a version stable enough to cite as a research object.

## License

The framework is licensed under `MIT`. The license permits use, modification, publication, distribution, sublicensing, and commercial use. Copies or substantial portions must retain the copyright and permission notice. MIT does not require derivatives to publish their source or retain the same license.

The repository contains a textual framework, operational templates, and may later include code. MIT was chosen to make practical reuse simple. This note is not legal advice.

## Authorship and provenance

The cited authors are **Denisa Faltová & Mark**. [`AUTHORS.md`](AUTHORS.md) describes their distinct contributions. `CITATION.cff` provides machine-readable citation metadata. The MIT copyright notice names Denisa Faltová as the human rights holder and the person able to grant the license.

Publishing the internal dialogue, personal continuity, or private source material is not necessary for truthful disclosure of the collaboration. Before accepting external contributions, the maintainers can decide who approves changes and who may issue a release.

## Operational sources

- [GitHub: About README files](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- [GitHub: Licensing a repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
- [GitHub: About CITATION files](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)
- [GitHub Pages: Creating a site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Zenodo: GitHub integration](https://help.zenodo.org/docs/github/)
- [Zenodo: Archive a GitHub release](https://help.zenodo.org/docs/github/archive-software/github-upload/)

