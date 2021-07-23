## Autopartes

This is an exact copy of the original repo. The only change is the renaming of the original [README.md](./README_original.md) into this file.

This repository is not necessary as Autopartes does not require any changes to this repo. We can use the original [reaction-development-platform repository](https://github.com/reactioncommerce/reaction-development-platform) instead.

The only 100% required repository is the [Autopartes Store-Front replacement](https://github.com/weknowinc/autopartes) which used as based [example-storefront](https://github.com/reactioncommerce/example-storefront) v3.0.0.

We also have the [autopartes-proxy-traefik](https://github.com/weknowinc/autopartes-proxy-traefik) which is a fork of the original [proxy-traefik repository](https://github.com/reactioncommerce/proxy-traefik). This repo has changes to adapt the deploy to our needs (mainly the playbook files). But I guess I would rather pack that into the autopartes repository and have only one. To be fair it doesn't add much, it is mainly an split of the playbook as is too long and there can be errors in the process. Also some steps are the make/git download/build which can fail and in my opinion is a bit overkill to put it within the playbook. I would simply split the original playbook in to and run that step manually as we do in local.

There is a VERY small change which was done here:

```
git diff config.mk
	...
	 https://github.com/reactioncommerce/reaction-admin.git,reaction-admin,v3.0.0-beta.7 \
	-https://github.com/reactioncommerce/example-storefront.git,example-storefront,v3.1.0
	+git@github.com:weknowinc/autopartes.git,autopartes,master
```

But this step is explained in the [setup section of the autopartes repository](https://github.com/weknowinc/autopartes#setup).
