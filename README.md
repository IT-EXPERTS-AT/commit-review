## Testing

Run locally using [act](https://github.com/nektos/act).
Some commands might not be found like `gh` depending on the container you use

```
act -e push.json
```

## Info

Every commit to the `main` branch will be checked on keyword changes and if the mandatory reviewers have approved it.
They are defined in the [commit-review.yml](./.github.com/workflows/commit-review.yml).
The reviewers are assigned using their github usernames.

The workflow will create a PR for that change and assign the reviewers.
If the changes were merged with a PR then only the missing mandatory reviewers will be added.
