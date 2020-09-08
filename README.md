# Important notice!

This project now realizes its work with https://developer.overheid.nl (DON). Reason: why create another place to support co-creation? Let's co-create in an existing and well known project such as DON.

So visit https://gitlab.com/commonground/developer.overheid.nl to see the results of this initiative.

# GovHub

## System overview

![System overview diagram](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.github.com/openstate/govhub/master/docs/system_overview.puml)
- Periodic link checker will also check if the OpenAPI equals the OpenAPI source in git, if not the git is updated with the new OpenAPI source
- Creation of new projects or updates on OpenAPI specification will trigger a webhook call to the PWA
- PWA will fetch OpenAPI source specs & apply [JSON patches](http://jsonpatch.com/) (after webhook call) from git with API
- PWA will fetch latest comments from Discourse with API
