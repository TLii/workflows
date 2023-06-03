# workflows
## check_upstream_head
Checks upstream repository for last commit id and outputs true if it differs from recorded onw.
### Inputs
- `upstream_repo`: (**required**) Upstream git repository address, preferrably http
- `upstream_branch`: (**required**) The branch name in upstream to monitor
- `ci_dir`: (optional) Location of CI data within repository running this workflow. Default is `.ci`
### Outputs
- `upstream_head`: The current HEAD commit id in upstream branch
- `upstream_changed`: True if the said commit id differs from the one recorded in `$ci_dir/upstream.head.txt`.
### Limitations:
- Works only with public upstreams for now
- **Workflow doesn't record commit id**. This is by design. Pipeline must record the new head commit from output.