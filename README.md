# silverstripe-cloud-dash-action

This action interacts with the Silverstripe Cloud Dashboard API.

Currently creates a deployment for the commit SHA that triggered the
workflow.

## Inputs

### dash-api-username [Required]

(Usually) email address of the user you will be authenticating as.

### dash-api-token [Required]

API token generated from your profile that allows you to interact with 
the dashboard

### dash-stack-name [Required]

Short name for your stack (check the URL in Dash). Maximum 8 characters

### dash-env-name [Required]

Which environment to interact with (usually UAT or Production)

### debug

Show debug output

## Development

### Requirements

- `yarn`
- `ncc` installed globally

### Changes

Use the `develop` branch for changes. Make your edits in `index.js`, but make
sure you run `yarn build` before committing, as the file in `dist/index.js`
is what is actually read when the action is run.

Use semver for tagging and releases.

## TODOs

- split out a core library for Dash access and re-use it for a CWP version
- make things a little more customisable
    - fill in description somehow
    - allow different 'bypass' types
    - custom deploy titles
