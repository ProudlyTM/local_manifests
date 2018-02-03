## To duplicate:

```
curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/proudlytm/local_manifests/dot-o/local_manifest.xml
```

## To sync:

```
repo sync -c -j4 --force-sync --no-clone-bundle --no-tags
```

## After syncing:
```
rm -rf vendor/qcom/opensource/dataservices
```
