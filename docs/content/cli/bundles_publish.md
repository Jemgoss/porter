---
title: "porter bundles publish"
slug: porter_bundles_publish
url: /cli/porter_bundles_publish/
---
## porter bundles publish

Publish a bundle

### Synopsis

Publishes a bundle by pushing the invocation image and bundle to a registry.

Note: if overrides for registry/tag/reference are provided, this command only re-tags the invocation image and bundle; it does not re-build the bundle.

```
porter bundles publish [flags]
```

### Examples

```
  porter bundle publish
  porter bundle publish --file myapp/porter.yaml
  porter bundle publish --dir myapp
  porter bundle publish --archive /tmp/mybuns.tgz --reference myrepo/my-buns:0.1.0
  porter bundle publish --tag latest
  porter bundle publish --registry myregistry.com/myorg
		
```

### Options

```
  -a, --archive string      Path to the bundle archive in .tgz format
  -d, --dir string          Path to the build context directory where all bundle assets are located.
  -f, --file porter.yaml    Path to the Porter manifest. Defaults to porter.yaml in the current directory.
  -h, --help                help for publish
      --insecure-registry   Don't require TLS for the registry
  -r, --reference string    Use a bundle in an OCI registry specified by the given reference.
      --registry string     Override the registry portion of the bundle reference, e.g. docker.io, myregistry.com/myorg
      --tag string          Override the Docker tag portion of the bundle reference, e.g. latest, v0.1.1
```

### Options inherited from parent commands

```
      --debug                  Enable debug logging
      --debug-plugins          Enable plugin debug logging
      --experimental strings   Comma separated list of experimental features to enable. See https://porter.sh/configuration/#experimental-feature-flags for available feature flags.
```

### SEE ALSO

* [porter bundles](/cli/porter_bundles/)	 - Bundle commands

