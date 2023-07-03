# workflows
This repository hosts my reusable workflows and workflow templates. Use them if you wish, but please understand I will not provide any support. Workflows might also change at any time.
## check_upstream_head
Checks upstream repository for last commit id and outputs true if it differs from recorded onw.
### Inputs
- `upstream_repo`: (**required**) Upstream git repository address, preferrably http
- `upstream_branch`: (**required**) The branch name in upstream to monitor
- `last_upstream_head`: The head id that current head  should be compared to. Can be either the id string itself or (relative) path to a file recording it (and nothing else).
### Outputs
- `upstream_head`: The current HEAD commit id in upstream branch
- `upstream_changed`: True if the said commit id differs from the one recorded in `$ci_dir/upstream.head.txt`.
### Limitations:
- Works only with public upstreams for now
## validate
Validate source code
### Inputs
See workflow file.
### Outputs
None.
### Limitations
