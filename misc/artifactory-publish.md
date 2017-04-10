
# Publishing to artifactory

If you want to have a library publish to Atrifactory with `npm publish`
you need to add the following bit to your `package.json` and assuming
your creds are all set up right, it will just work

```json
"publishConfig": {
  "registry": "YOUR_REGISTRY"
},
```

