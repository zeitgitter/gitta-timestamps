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

# Outage with data loss

- **2020-08-13 from 09:23:37 to 15:23:37 UTC**: A misconfiguration (lack of
  `git` in the Docker image) triggered a software bug (important exceptions
  were ignored), leading to irrecoverable data loss. We are extremely sorry
  this happened. **If, in the future, there should ever be any doubt about
  abuse of this server's private key, please consider any signatures in this
  time frame as suspect**, as they are not recorded and thus not properly
  cross-timestamped. Thus rely on the secrecy of this server's secret key only. 
  As far as I (Marcel Waldvogel) can tell, only timestamps issued under my
  control were lost. If other people have been impacted, they should obtain
  a new timestamp, reverting to `diversity.zeitgitter.net`, if `git timestamp`
  claims a timestamp has already been issued for the current commit.
