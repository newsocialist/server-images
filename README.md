# server-images

Install [Packer](https://www.packer.io).

Add sensitive files to the `/user` directory, which is ignored by Git.


```
$ ls -1 user
authorized_keys
vars.json
```

Check the config is ok:

```
$ packer validate -var-file=user/vars.json web.json
```

Build snapshot:

```
$ packer build -var-file=user/vars.json web.json
```
