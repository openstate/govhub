# GovHub

## System overview

![System overview diagram](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.github.com/openstate/govhub/master/docs/system_overview.puml)
- Periodic link checker will also check if the OpenAPI equals the OpenAPI source in git, if not the git is updated with the new OpenAPI source
- Creation of new projects or updates on OpenAPI specification will trigger a webhook call to the PWA
- PWA will fetch OpenAPI source specs & apply patches (after webhook call) from git with API
- PWA will fetch latest comments from Discourse with API
