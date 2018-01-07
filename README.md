To duplicate:

```
curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/proudlytm/local_manifests/lineage-15.1/local_manifest.xml
```

To sync:

```
repo sync --force-sync
```
