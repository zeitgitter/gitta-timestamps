# Timestamping log for `gitta.zeitgitter.net`

This lists all commit IDs for which
[`gitta.zeitgitter.net`](https://gitta.zeitgitter.net) (previously known as
`gitta.enotar.ch`) has ever issued a timestamp
signature. If there are any other signatures, please do consider them invalid.

This is part of the *Zeitgitter* distributed timestamping system. Please learn more
about *Zeitgitter* at https://zeitgitter.net .

# Verify timestamping log

To verify whether a given commit is in there, e.g., one dated at `2019-04-01
19:30`, please use the following commands on a checked-out copy of this repository:

```sh
git checkout `git rev-list --since="2019-04-01 19:30" --reverse master | head -1`
```

You should be able to find the commit ID in `hashes.log` then.
