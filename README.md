# scoop-bucket

A [Scoop](https://scoop.sh) bucket for Merbac's Windows apps.

```powershell
scoop bucket add merbac https://github.com/mercibac/scoop-bucket
```

## Apps

| App | What it is |
| --- | --- |
| [gig-center](https://github.com/mercibac/gig-center) | Gig Control Center — live performance setup automation |

```powershell
scoop install gig-center
```

`scoop update gig-center` from then on.

## How the manifests get here

They are not written by hand. The release workflow in each app's own
repository rewrites its manifest when a version ships, hashing the file the
release actually serves rather than the local build — so a manifest here can
only ever describe a download that exists.

Manifests live in `bucket/`, which is where Scoop's own `Find-BucketDirectory`
looks before falling back to the repository root.
