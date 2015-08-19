```
chef generate cookbook ultraman
cd ultraman
git add .
git commit -m 'initial commit of ultraman'
delivery init --local
delivery job verify "lint syntax unit" --local
```

```
cd ultraman/.delivery/build-cookbook
kitchen list
kitchen converge default-centos-71
```
