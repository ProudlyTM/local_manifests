To duplicate:

```
curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/proudlytm/local_manifests/lineage-15.1/local_manifest.xml
```

To sync:

```
repo sync -c -j4 --force-sync --no-clone-bundle --no-tags
```

After syncing:
```
rm -rf vendor/qcom/opensource/dataservices
export ALLOW_MISSING_DEPENDENCIES=true
cd system/qcom && curl 'https://github.com/LineageOS/android_system_qcom/commit/07e73ebcc98757b2b4a8f863128961caffeaced8.patch' > patch && git apply patch && rm patch
```
