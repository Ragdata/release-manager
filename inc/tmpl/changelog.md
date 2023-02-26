{{#doc header}}
# {{name}} CHANGELOG

All notable changes in this project will be documented in this file.  

See [Release Manager Contributor's Guidelines](https://github.com/Ragdata/.github/blob/master/.github/CONTRIBUTING.md) for commit message requirements.

{{/doc header}}
{{#doc body}}
{{#each releases}}

## [{{release_version}}]({{release_url}}) ({{release_date}})

{{#each sections}}

### {{type_icon}} {{type_title}}

{{type_description}}

{{#each commits}}
* {{#if commit_scope}}({{commit_scope}}) {{/if}}{{commit_subject}} [{{commit_ref}}]({{commit_url}})
{{#if commit_body}}  * {{commit_body}}{{/if}}{{#if commit_footer}}<br />{{commit_footer}}{{/if}}
{{/each commits}}

{{/each sections}}

{{/each releases}}
{{/doc body}}
{{#doc footer}}

Changelog last updated on {{date_today}} for [{{name}}]({{repo_url}}) by [Release Manager](https://github.com/ragdata/release-manager)
{{/doc footer}}
