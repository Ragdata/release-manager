# {{prettyName}} CHANGELOG

All notable changes in this project will be documented in this file.  See [Release Manager](https://github.com/ragdata/release-manager) for commit guidelines.

{{#each releases}}
## [{{release_version}}]({{release_url}}) ({{release_date}})

{{#each sections}}
### {{type_icon}} {{type_title}}

{{type_description}}

{{#each commits}}
* {{#if commit_scope not empty}}({{commit_scope}}) {{/if}}{{commit_subject}} [{{commit_ref}}]({{commit_url}})
{{#if commit_body not empty}}  * {{commit_body}}{{/if}}{{#if commit_footer not empty}}<br />{{commit_footer}}{{/if}}
{{/each}}
{{/each}}
{{/each}}

Changelog last updated on {{date_today}} for [{{prettyName}}]({{repo_url}}) by [Release Manager](https://github.com/ragdata/release-manager)